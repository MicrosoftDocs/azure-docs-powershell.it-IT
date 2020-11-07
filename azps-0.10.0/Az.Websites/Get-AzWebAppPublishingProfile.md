---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 477b60400082954eb12bd0756fb4380ece2a35ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861921"
---
# <span data-ttu-id="b7180-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b7180-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="b7180-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7180-102">SYNOPSIS</span></span>
<span data-ttu-id="b7180-103">Ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b7180-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="b7180-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7180-104">SYNTAX</span></span>

### <span data-ttu-id="b7180-105">S1</span><span class="sxs-lookup"><span data-stu-id="b7180-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7180-106">S2</span><span class="sxs-lookup"><span data-stu-id="b7180-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7180-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7180-107">DESCRIPTION</span></span>
<span data-ttu-id="b7180-108">Il cmdlet **Get-AzWebAppPublishingProfile** ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b7180-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="b7180-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7180-109">EXAMPLES</span></span>

### <span data-ttu-id="b7180-110">1:</span><span class="sxs-lookup"><span data-stu-id="b7180-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="b7180-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="b7180-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="b7180-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7180-112">PARAMETERS</span></span>

### <span data-ttu-id="b7180-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7180-113">-DefaultProfile</span></span>
<span data-ttu-id="b7180-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7180-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7180-115">-Format</span><span class="sxs-lookup"><span data-stu-id="b7180-115">-Format</span></span>
<span data-ttu-id="b7180-116">Formato</span><span class="sxs-lookup"><span data-stu-id="b7180-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7180-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7180-117">-Name</span></span>
<span data-ttu-id="b7180-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="b7180-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7180-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="b7180-119">-OutputFile</span></span>
<span data-ttu-id="b7180-120">File di output</span><span class="sxs-lookup"><span data-stu-id="b7180-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7180-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7180-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7180-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b7180-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7180-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="b7180-123">-WebApp</span></span>
<span data-ttu-id="b7180-124">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="b7180-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7180-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7180-125">CommonParameters</span></span>
<span data-ttu-id="b7180-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7180-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7180-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7180-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7180-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7180-128">INPUTS</span></span>

### <span data-ttu-id="b7180-129">Sito</span><span class="sxs-lookup"><span data-stu-id="b7180-129">Site</span></span>
<span data-ttu-id="b7180-130">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="b7180-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b7180-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7180-131">OUTPUTS</span></span>

## <span data-ttu-id="b7180-132">Note</span><span class="sxs-lookup"><span data-stu-id="b7180-132">NOTES</span></span>

## <span data-ttu-id="b7180-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7180-133">RELATED LINKS</span></span>

[<span data-ttu-id="b7180-134">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b7180-134">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="b7180-135">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b7180-135">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


