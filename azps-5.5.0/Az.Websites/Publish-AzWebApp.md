---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207458"
---
# <span data-ttu-id="309ae-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="309ae-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="309ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="309ae-102">SYNOPSIS</span></span>
<span data-ttu-id="309ae-103">Distribuisce un'app Web di Azure da un file ZIP, JAR o WAR con zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="309ae-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="309ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="309ae-104">SYNTAX</span></span>

### <span data-ttu-id="309ae-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="309ae-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="309ae-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="309ae-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="309ae-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="309ae-107">DESCRIPTION</span></span>
<span data-ttu-id="309ae-108">Il cmdlet **Publish-AzWebApp** carica il contenuto in un'app Web di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="309ae-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="309ae-109">Il contenuto deve essere in un pacchetto in un file ZIP se si usano stack come .NET, Python o Node oppure un file WAR o JAR se si usa Java.</span><span class="sxs-lookup"><span data-stu-id="309ae-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="309ae-110">Il contenuto deve essere predefinito e pronto per l'esecuzione senza altri passaggi di build durante la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="309ae-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="309ae-111">Questo cmdlet usa le caratteristiche Kudu zipdeploy e wardeploy per distribuire il contenuto.</span><span class="sxs-lookup"><span data-stu-id="309ae-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="309ae-112">Vedere il wiki Kudu per informazioni dettagliate sul funzionamento di zipdeploy e wardeploy e su come creare correttamente il pacchetto di un'app Web per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="309ae-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="309ae-113"> https://aka.ms/kuduzipdeploy e https://aka.ms/kuduwardeploy contengono informazioni utili sulla zipdeploy e la wardeploy.</span><span class="sxs-lookup"><span data-stu-id="309ae-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="309ae-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="309ae-114">EXAMPLES</span></span>

### <span data-ttu-id="309ae-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="309ae-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="309ae-116">Carica il contenuto della app.zip'app Web denominata MyApp appartenente al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="309ae-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="309ae-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="309ae-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="309ae-118">Carica il contenuto di javaproject.war nello slot di gestione dell'app Web denominato ContosoApp appartenente al gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="309ae-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="309ae-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="309ae-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="309ae-120">Carica il contenuto della app.zip'app Web denominata ContosoApp appartenente al gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="309ae-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="309ae-121">Il cmdlet verrà eseguito in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="309ae-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="309ae-122">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="309ae-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="309ae-123">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="309ae-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="309ae-124">Carica il contenuto di java_app.jar nell'app Web denominata ContosoApp appartenente al gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="309ae-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="309ae-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="309ae-125">PARAMETERS</span></span>

### <span data-ttu-id="309ae-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="309ae-126">-ArchivePath</span></span>
<span data-ttu-id="309ae-127">Percorso del file di archivio.</span><span class="sxs-lookup"><span data-stu-id="309ae-127">The path of the archive file.</span></span> <span data-ttu-id="309ae-128">Zip, WAR e JAR sono supportati.</span><span class="sxs-lookup"><span data-stu-id="309ae-128">ZIP, WAR, and JAR are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ae-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="309ae-129">-AsJob</span></span>
<span data-ttu-id="309ae-130">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="309ae-130">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ae-131">-Force</span><span class="sxs-lookup"><span data-stu-id="309ae-131">-Force</span></span>
<span data-ttu-id="309ae-132">Opzione Rimuovi forzatamente</span><span class="sxs-lookup"><span data-stu-id="309ae-132">Forcefully Remove Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ae-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="309ae-133">-DefaultProfile</span></span>
<span data-ttu-id="309ae-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="309ae-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="309ae-135">-Name</span><span class="sxs-lookup"><span data-stu-id="309ae-135">-Name</span></span>
<span data-ttu-id="309ae-136">Il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="309ae-136">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="309ae-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="309ae-137">-ResourceGroupName</span></span>
<span data-ttu-id="309ae-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="309ae-138">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="309ae-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="309ae-139">-Slot</span></span>
<span data-ttu-id="309ae-140">Nome dello slot dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="309ae-140">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="309ae-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="309ae-141">-WebApp</span></span>
<span data-ttu-id="309ae-142">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="309ae-142">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="309ae-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="309ae-143">CommonParameters</span></span>
<span data-ttu-id="309ae-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="309ae-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="309ae-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="309ae-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="309ae-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="309ae-146">INPUTS</span></span>

### <span data-ttu-id="309ae-147">System.String</span><span class="sxs-lookup"><span data-stu-id="309ae-147">System.String</span></span>

### <span data-ttu-id="309ae-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="309ae-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="309ae-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="309ae-149">OUTPUTS</span></span>

### <span data-ttu-id="309ae-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="309ae-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="309ae-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="309ae-151">NOTES</span></span>

## <span data-ttu-id="309ae-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="309ae-152">RELATED LINKS</span></span>
