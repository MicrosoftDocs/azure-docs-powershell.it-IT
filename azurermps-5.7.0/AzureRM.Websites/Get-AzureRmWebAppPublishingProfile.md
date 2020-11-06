---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 1202d15504717052513f1ef77a21e008fefe20af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509519"
---
# <span data-ttu-id="4c14e-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="4c14e-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="4c14e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c14e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c14e-103">Ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4c14e-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c14e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c14e-104">SYNTAX</span></span>

### <span data-ttu-id="4c14e-105">S1</span><span class="sxs-lookup"><span data-stu-id="4c14e-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c14e-106">S2</span><span class="sxs-lookup"><span data-stu-id="4c14e-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c14e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c14e-107">DESCRIPTION</span></span>
<span data-ttu-id="4c14e-108">Il cmdlet **Get-AzureRmWebAppPublishingProfile** ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4c14e-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="4c14e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c14e-109">EXAMPLES</span></span>

### <span data-ttu-id="4c14e-110">1:</span><span class="sxs-lookup"><span data-stu-id="4c14e-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="4c14e-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="4c14e-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="4c14e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c14e-112">PARAMETERS</span></span>

### <span data-ttu-id="4c14e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c14e-113">-DefaultProfile</span></span>
<span data-ttu-id="4c14e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c14e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c14e-115">-Format</span><span class="sxs-lookup"><span data-stu-id="4c14e-115">-Format</span></span>
<span data-ttu-id="4c14e-116">Formato</span><span class="sxs-lookup"><span data-stu-id="4c14e-116">Format</span></span>

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

### <span data-ttu-id="4c14e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c14e-117">-Name</span></span>
<span data-ttu-id="4c14e-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="4c14e-118">WebApp Name</span></span>

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

### <span data-ttu-id="4c14e-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="4c14e-119">-OutputFile</span></span>
<span data-ttu-id="4c14e-120">File di output</span><span class="sxs-lookup"><span data-stu-id="4c14e-120">Output File</span></span>

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

### <span data-ttu-id="4c14e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c14e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4c14e-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4c14e-122">Resource Group Name</span></span>

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

### <span data-ttu-id="4c14e-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="4c14e-123">-WebApp</span></span>
<span data-ttu-id="4c14e-124">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="4c14e-124">WebApp Object</span></span>

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

### <span data-ttu-id="4c14e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c14e-125">CommonParameters</span></span>
<span data-ttu-id="4c14e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c14e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c14e-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c14e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c14e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c14e-128">INPUTS</span></span>

### <span data-ttu-id="4c14e-129">Sito</span><span class="sxs-lookup"><span data-stu-id="4c14e-129">Site</span></span>
<span data-ttu-id="4c14e-130">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4c14e-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4c14e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c14e-131">OUTPUTS</span></span>

## <span data-ttu-id="4c14e-132">Note</span><span class="sxs-lookup"><span data-stu-id="4c14e-132">NOTES</span></span>

## <span data-ttu-id="4c14e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c14e-133">RELATED LINKS</span></span>

[<span data-ttu-id="4c14e-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4c14e-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="4c14e-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4c14e-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


