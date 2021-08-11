import mu.KotlinLogging
import org.dom4j.Document
import org.dom4j.DocumentException //lib necessária
import org.dom4j.Element
import org.dom4j.io.SAXReader
import java.io.File
import java.io.FileWriter
import java.nio.charset.Charset
import java.util.*


class EditaSvgKotlin {

    private val log = KotlinLogging.logger {}

    @Throws(DocumentException::class)
    fun parse(url: String?): Document? {
        val reader = SAXReader()
        return reader.read(File(url).reader(Charset.defaultCharset()))
    }

    fun carregaArquivo() {
    
    	//TROCAR A PALAVRA MUDA PELO ID QUE DESEJA ALTERAR
        //concertar diretório ao implementar
        val document = parse("./file.svg")
        val rootElm = document?.rootElement!!


        var dados: Optional<Element> = Optional.empty()
        if (rootElm != null) {
           // EM CASO DE DUVIDA PEGAR UM ELEMENTO E PRINTAR SEU UNIQUEPATH
           //val x=rootElm.selectSingleNode( "//svg")
           //val list2 = document.selectNodes("/*[name()='svg']/*[name()='g']/*")
           //document.selectNodes("//*[name()='g']//*[name()='span']")----------------------------OTRNAS TODOS OS SPANS
           //val list = document.selectNodes("//svg/*")
           // val list2 = document.selectNodes("//*[@id='MUDA']")
           
            var element= (document.selectSingleNode("//*[@id='MUDA']"))


           element!!.text="EUMUDEI"
            val out = FileWriter("foo.svg")
            document.write(out)
            out.close()
        }
     
    }

}
