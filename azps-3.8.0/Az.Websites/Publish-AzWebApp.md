---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018690"
---
# <span data-ttu-id="3ee79-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3ee79-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="3ee79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ee79-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee79-103">Distribuisce un'app Azure Web da un file ZIP, JAR o WAR usando zipdeploy.</span><span class="sxs-lookup"><span data-stu-id="3ee79-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="3ee79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ee79-104">SYNTAX</span></span>

### <span data-ttu-id="3ee79-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="3ee79-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee79-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="3ee79-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="3ee79-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ee79-107">DESCRIPTION</span></span>
<span data-ttu-id="3ee79-108">Il cmdlet **Publish-AzWebApp** carica il contenuto in un'app Web Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="3ee79-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="3ee79-109">Il contenuto deve essere assemblato in un file ZIP se si usano pile come .NET, Python o node oppure un file WAR o JAR se si usa Java.</span><span class="sxs-lookup"><span data-stu-id="3ee79-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="3ee79-110">Il contenuto deve essere pre-compilato e pronto per l'esecuzione senza ulteriori passaggi di compilazione durante la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3ee79-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="3ee79-111">Questo cmdlet usa le caratteristiche zipdeploy e wardeploy di Kudu per distribuire contenuto.</span><span class="sxs-lookup"><span data-stu-id="3ee79-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="3ee79-112">Vedere il wiki di Kudu per informazioni dettagliate sul funzionamento di zipdeploy e wardeploy e su come assemblare correttamente un'app Web per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="3ee79-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="3ee79-113"> https://aka.ms/kuduzipdeploy e https://aka.ms/kuduwardeploy contengono informazioni utili su zipdeploy e wardeploy.</span><span class="sxs-lookup"><span data-stu-id="3ee79-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="3ee79-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ee79-114">EXAMPLES</span></span>

### <span data-ttu-id="3ee79-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ee79-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="3ee79-116">Carica il contenuto di app.zip nell'app Web denominata MyApp che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="3ee79-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="3ee79-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3ee79-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="3ee79-118">Carica il contenuto di javaproject. War nello slot di staging dell'app Web denominata ContosoApp appartenente al gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="3ee79-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="3ee79-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3ee79-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="3ee79-120">Carica il contenuto di app.zip nell'app Web denominata ContosoApp appartenente al gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="3ee79-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="3ee79-121">Il cmdlet verrà eseguito in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="3ee79-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="3ee79-122">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="3ee79-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="3ee79-123">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="3ee79-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="3ee79-124">Carica il contenuto di java_app. jar nell'app Web denominata ContosoApp appartenente al gruppo di risorse ContosoRG.</span><span class="sxs-lookup"><span data-stu-id="3ee79-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="3ee79-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ee79-125">PARAMETERS</span></span>

### <span data-ttu-id="3ee79-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="3ee79-126">-ArchivePath</span></span>
<span data-ttu-id="3ee79-127">Percorso del file di archivio.</span><span class="sxs-lookup"><span data-stu-id="3ee79-127">The path of the archive file.</span></span> <span data-ttu-id="3ee79-128">Sono supportati ZIP, WAR e JAR.</span><span class="sxs-lookup"><span data-stu-id="3ee79-128">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="3ee79-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ee79-129">-AsJob</span></span>
<span data-ttu-id="3ee79-130">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3ee79-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ee79-131">-Force</span><span class="sxs-lookup"><span data-stu-id="3ee79-131">-Force</span></span>
<span data-ttu-id="3ee79-132">Opzione Rimuovi con forza</span><span class="sxs-lookup"><span data-stu-id="3ee79-132">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="3ee79-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee79-133">-DefaultProfile</span></span>
<span data-ttu-id="3ee79-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee79-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ee79-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ee79-135">-Name</span></span>
<span data-ttu-id="3ee79-136">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="3ee79-136">The name of the web app.</span></span>

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

### <span data-ttu-id="3ee79-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee79-137">-ResourceGroupName</span></span>
<span data-ttu-id="3ee79-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ee79-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ee79-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="3ee79-139">-Slot</span></span>
<span data-ttu-id="3ee79-140">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="3ee79-140">The name of the web app slot.</span></span>

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

### <span data-ttu-id="3ee79-141">-Web App</span><span class="sxs-lookup"><span data-stu-id="3ee79-141">-WebApp</span></span>
<span data-ttu-id="3ee79-142">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="3ee79-142">The web app object</span></span>

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

### <span data-ttu-id="3ee79-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee79-143">CommonParameters</span></span>
<span data-ttu-id="3ee79-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee79-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee79-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee79-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee79-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ee79-146">INPUTS</span></span>

### <span data-ttu-id="3ee79-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3ee79-147">System.String</span></span>

### <span data-ttu-id="3ee79-148">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3ee79-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3ee79-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ee79-149">OUTPUTS</span></span>

### <span data-ttu-id="3ee79-150">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3ee79-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3ee79-151">Note</span><span class="sxs-lookup"><span data-stu-id="3ee79-151">NOTES</span></span>

## <span data-ttu-id="3ee79-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ee79-152">RELATED LINKS</span></span>
