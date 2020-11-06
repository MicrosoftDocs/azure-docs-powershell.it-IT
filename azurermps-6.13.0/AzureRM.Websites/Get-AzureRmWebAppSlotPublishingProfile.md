---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 29ef83bf3ed0f423686e7ddf84bc82555bd09572
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507248"
---
# <span data-ttu-id="ad0bd-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ad0bd-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="ad0bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0bd-103">Ottiene un profilo di pubblicazione dello slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ad0bd-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad0bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad0bd-104">SYNTAX</span></span>

### <span data-ttu-id="ad0bd-105">S1</span><span class="sxs-lookup"><span data-stu-id="ad0bd-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad0bd-106">S2</span><span class="sxs-lookup"><span data-stu-id="ad0bd-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad0bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad0bd-107">DESCRIPTION</span></span>
<span data-ttu-id="ad0bd-108">Il cmdlet **Get-AzureRmWebAppSlotPublishingProfile** ottiene il profilo di pubblicazione dell'app Web per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="ad0bd-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="ad0bd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad0bd-109">EXAMPLES</span></span>

### <span data-ttu-id="ad0bd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad0bd-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="ad0bd-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="ad0bd-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="ad0bd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad0bd-112">PARAMETERS</span></span>

### <span data-ttu-id="ad0bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0bd-113">-DefaultProfile</span></span>
<span data-ttu-id="ad0bd-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad0bd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad0bd-115">-Format</span><span class="sxs-lookup"><span data-stu-id="ad0bd-115">-Format</span></span>
<span data-ttu-id="ad0bd-116">Formato</span><span class="sxs-lookup"><span data-stu-id="ad0bd-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0bd-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="ad0bd-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="ad0bd-118">Includere gli endpoint di ripristino di emergenza se vero</span><span class="sxs-lookup"><span data-stu-id="ad0bd-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="ad0bd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad0bd-119">-Name</span></span>
<span data-ttu-id="ad0bd-120">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ad0bd-120">WebApp Name</span></span>

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

### <span data-ttu-id="ad0bd-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ad0bd-121">-OutputFile</span></span>
<span data-ttu-id="ad0bd-122">File di output</span><span class="sxs-lookup"><span data-stu-id="ad0bd-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad0bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad0bd-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ad0bd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ad0bd-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="ad0bd-125">-Slot</span></span>
<span data-ttu-id="ad0bd-126">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="ad0bd-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad0bd-127">-Web App</span><span class="sxs-lookup"><span data-stu-id="ad0bd-127">-WebApp</span></span>
<span data-ttu-id="ad0bd-128">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ad0bd-128">WebApp Object</span></span>

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

### <span data-ttu-id="ad0bd-129">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="ad0bd-129">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="ad0bd-130">Includere gli endpoint di ripristino di emergenza se vero</span><span class="sxs-lookup"><span data-stu-id="ad0bd-130">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="ad0bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0bd-131">CommonParameters</span></span>
<span data-ttu-id="ad0bd-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad0bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad0bd-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad0bd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0bd-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad0bd-134">INPUTS</span></span>

### <span data-ttu-id="ad0bd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ad0bd-135">System.String</span></span>

### <span data-ttu-id="ad0bd-136">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="ad0bd-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ad0bd-137">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad0bd-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ad0bd-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad0bd-138">OUTPUTS</span></span>

### <span data-ttu-id="ad0bd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ad0bd-139">System.String</span></span>

## <span data-ttu-id="ad0bd-140">Note</span><span class="sxs-lookup"><span data-stu-id="ad0bd-140">NOTES</span></span>

## <span data-ttu-id="ad0bd-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad0bd-141">RELATED LINKS</span></span>

[<span data-ttu-id="ad0bd-142">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ad0bd-142">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="ad0bd-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad0bd-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad0bd-144">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad0bd-144">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
