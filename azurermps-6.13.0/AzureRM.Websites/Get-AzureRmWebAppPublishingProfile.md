---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513299"
---
# <span data-ttu-id="ba953-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ba953-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="ba953-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba953-102">SYNOPSIS</span></span>
<span data-ttu-id="ba953-103">Ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ba953-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba953-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba953-104">SYNTAX</span></span>

### <span data-ttu-id="ba953-105">S1</span><span class="sxs-lookup"><span data-stu-id="ba953-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba953-106">S2</span><span class="sxs-lookup"><span data-stu-id="ba953-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba953-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba953-107">DESCRIPTION</span></span>
<span data-ttu-id="ba953-108">Il cmdlet **Get-AzureRmWebAppPublishingProfile** ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ba953-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="ba953-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba953-109">EXAMPLES</span></span>

### <span data-ttu-id="ba953-110">1:</span><span class="sxs-lookup"><span data-stu-id="ba953-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="ba953-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="ba953-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="ba953-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba953-112">PARAMETERS</span></span>

### <span data-ttu-id="ba953-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba953-113">-DefaultProfile</span></span>
<span data-ttu-id="ba953-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba953-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba953-115">-Format</span><span class="sxs-lookup"><span data-stu-id="ba953-115">-Format</span></span>
<span data-ttu-id="ba953-116">Formato</span><span class="sxs-lookup"><span data-stu-id="ba953-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba953-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="ba953-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="ba953-118">Includere gli endpoint di ripristino di emergenza se vero</span><span class="sxs-lookup"><span data-stu-id="ba953-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba953-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba953-119">-Name</span></span>
<span data-ttu-id="ba953-120">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ba953-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba953-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ba953-121">-OutputFile</span></span>
<span data-ttu-id="ba953-122">File di output</span><span class="sxs-lookup"><span data-stu-id="ba953-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba953-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba953-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba953-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ba953-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba953-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="ba953-125">-WebApp</span></span>
<span data-ttu-id="ba953-126">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ba953-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba953-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="ba953-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="ba953-128">Includere gli endpoint di ripristino di emergenza se vero</span><span class="sxs-lookup"><span data-stu-id="ba953-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba953-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba953-129">CommonParameters</span></span>
<span data-ttu-id="ba953-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba953-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba953-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba953-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba953-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba953-132">INPUTS</span></span>

### <span data-ttu-id="ba953-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ba953-133">System.String</span></span>

### <span data-ttu-id="ba953-134">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ba953-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ba953-135">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba953-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ba953-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba953-136">OUTPUTS</span></span>

### <span data-ttu-id="ba953-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ba953-137">System.String</span></span>

## <span data-ttu-id="ba953-138">Note</span><span class="sxs-lookup"><span data-stu-id="ba953-138">NOTES</span></span>

## <span data-ttu-id="ba953-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba953-139">RELATED LINKS</span></span>

[<span data-ttu-id="ba953-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ba953-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="ba953-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ba953-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


