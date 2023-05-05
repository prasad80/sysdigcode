import org.junit.Test;
import org.junit.runner.RunWith;
import org.mockito.InjectMocks;
import org.mockito.junit.MockitoJUnitRunner;
import org.springframework.ui.Model;
import static org.junit.Assert.assertEquals;
import static org.mockito.Mockito.mock;

@RunWith(MockitoJUnitRunner.class)
public class StartApplicationTest {

    @InjectMocks
    private StartApplication startApplication;

    @Test
    public void testIndex() {
        Model model = mock(Model.class);
        String result = startApplication.index(model);
        assertEquals("index", result);
    }