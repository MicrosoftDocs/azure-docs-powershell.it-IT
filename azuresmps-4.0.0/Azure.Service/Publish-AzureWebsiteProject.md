---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023835"
---
# <span data-ttu-id="1060d-101">Publish-AzureWebsiteProject</span><span class="sxs-lookup"><span data-stu-id="1060d-101">Publish-AzureWebsiteProject</span></span>

## <span data-ttu-id="1060d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1060d-102">SYNOPSIS</span></span>
<span data-ttu-id="1060d-103">Pubblicare un progetto Web di Visual Studio in un sito Web di Microsoft Azure tramite WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1060d-103">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>

## <span data-ttu-id="1060d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1060d-104">SYNTAX</span></span>

### <span data-ttu-id="1060d-105">ProjectFile</span><span class="sxs-lookup"><span data-stu-id="1060d-105">ProjectFile</span></span>
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="1060d-106">Pacchetto</span><span class="sxs-lookup"><span data-stu-id="1060d-106">Package</span></span>
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1060d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1060d-107">DESCRIPTION</span></span>
<span data-ttu-id="1060d-108">Pubblicare un progetto Web di Visual Studio in un sito Web di Microsoft Azure tramite WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1060d-108">Publish a Visual Studio web project to a Microsoft Azure web site using WebDeploy.</span></span>
<span data-ttu-id="1060d-109">Può prendere un pacchetto WebDeploy e pubblicarlo direttamente oppure creare un progetto Web di Visual Studio, compilare il progetto e pubblicarlo.</span><span class="sxs-lookup"><span data-stu-id="1060d-109">It can either take a WebDeploy package and publish directly, or take a Visual Studio web project, build the project and publish.</span></span>
<span data-ttu-id="1060d-110">Può anche sostituire le stringhe di connessione nel Web.config durante la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="1060d-110">It can also replace the connection strings in the Web.config during publish.</span></span>

## <span data-ttu-id="1060d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1060d-111">EXAMPLES</span></span>

### <span data-ttu-id="1060d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1060d-112">Example 1</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

<span data-ttu-id="1060d-113">Creare un progetto Web di Visual Studio con la configurazione "debug" (che significa usare Web.Debug.config) e pubblicare in un sito Web di Microsoft Azure tramite WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1060d-113">Build a Visual Studio web project with "Debug" configuration (meaning use Web.Debug.config) and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1060d-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1060d-114">Example 2</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

<span data-ttu-id="1060d-115">Pubblicare un file WebDeploy Package. zip in un sito Web di Microsoft Azure tramite WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1060d-115">Publish a WebDeploy Package .zip file to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1060d-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1060d-116">Example 3</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

<span data-ttu-id="1060d-117">Pubblicare una cartella del pacchetto WebDeploy in un sito Web di Microsoft Azure tramite WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1060d-117">Publish a WebDeploy Package folder to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1060d-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="1060d-118">Example 4</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

<span data-ttu-id="1060d-119">Creare un progetto Web di Visual Studio, sovrascrivere la stringa di connessione "DefaultConnection" in Web.config e pubblicarla in un sito Web di Microsoft Azure tramite WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1060d-119">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>

### <span data-ttu-id="1060d-120">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="1060d-120">Example 5</span></span>
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

<span data-ttu-id="1060d-121">Creare un progetto Web di Visual Studio, sovrascrivere la stringa di connessione "DefaultConnection" in Web.config e pubblicarla in un sito Web di Microsoft Azure tramite WebDeploy.</span><span class="sxs-lookup"><span data-stu-id="1060d-121">Build a Visual Studio web project, overwrite the "DefaultConnection" connection string in Web.config and publish to a Microsoft Azure Web Site using WebDeploy.</span></span>
<span data-ttu-id="1060d-122">Nota che-DefaultConnection è un parametro dinamico che viene aggiunto analizzando Web.config.</span><span class="sxs-lookup"><span data-stu-id="1060d-122">Notice that -DefaultConnection is a dynamic parameter which gets added by parsing Web.config.</span></span>

## <span data-ttu-id="1060d-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1060d-123">PARAMETERS</span></span>

### <span data-ttu-id="1060d-124">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="1060d-124">-Configuration</span></span>
<span data-ttu-id="1060d-125">La configurazione usata per compilare il progetto di applicazione Web di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1060d-125">The configuration used to build the Visual Studio web application project.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-126">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1060d-126">-ConnectionString</span></span>
<span data-ttu-id="1060d-127">Stringhe di connessione da usare per la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1060d-127">The connection strings to use for the deployment.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-128">-DoNotDelete</span><span class="sxs-lookup"><span data-stu-id="1060d-128">-DoNotDelete</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1060d-129">-Name</span></span>
<span data-ttu-id="1060d-130">Nome del sito Web.</span><span class="sxs-lookup"><span data-stu-id="1060d-130">The web site name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-131">-Pacchetto</span><span class="sxs-lookup"><span data-stu-id="1060d-131">-Package</span></span>
<span data-ttu-id="1060d-132">Cartella del pacchetto WebDeploy per il file zip del progetto di applicazione Web di Visual Studio da pubblicare.</span><span class="sxs-lookup"><span data-stu-id="1060d-132">The WebDeploy package folder for zip file of the Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="1060d-133">-Profile</span></span>
<span data-ttu-id="1060d-134">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1060d-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1060d-135">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1060d-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-136">-ProjectFile</span><span class="sxs-lookup"><span data-stu-id="1060d-136">-ProjectFile</span></span>
<span data-ttu-id="1060d-137">Progetto di applicazione Web di Visual Studio da pubblicare.</span><span class="sxs-lookup"><span data-stu-id="1060d-137">The Visual Studio web application project to be published.</span></span>

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-138">-SetParametersFile</span><span class="sxs-lookup"><span data-stu-id="1060d-138">-SetParametersFile</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-139">-SkipAppData</span><span class="sxs-lookup"><span data-stu-id="1060d-139">-SkipAppData</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="1060d-140">-Slot</span></span>
<span data-ttu-id="1060d-141">Nome dello slot del sito Web.</span><span class="sxs-lookup"><span data-stu-id="1060d-141">The web site slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-142">-Token</span><span class="sxs-lookup"><span data-stu-id="1060d-142">-Tokens</span></span>
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1060d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1060d-143">CommonParameters</span></span>
<span data-ttu-id="1060d-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1060d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1060d-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1060d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1060d-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1060d-146">INPUTS</span></span>

## <span data-ttu-id="1060d-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1060d-147">OUTPUTS</span></span>

## <span data-ttu-id="1060d-148">Note</span><span class="sxs-lookup"><span data-stu-id="1060d-148">NOTES</span></span>

## <span data-ttu-id="1060d-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1060d-149">RELATED LINKS</span></span>

[<span data-ttu-id="1060d-150">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1060d-150">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="1060d-151">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1060d-151">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="1060d-152">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1060d-152">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1060d-153">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1060d-153">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


