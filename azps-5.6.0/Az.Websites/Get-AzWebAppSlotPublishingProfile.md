---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: fed1be90af7aad2126b20dbe830f5069cc62e01f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994656"
---
# <span data-ttu-id="f566f-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f566f-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="f566f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f566f-102">SYNOPSIS</span></span>
<span data-ttu-id="f566f-103">Ottiene un profilo di pubblicazione degli slot per Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f566f-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="f566f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f566f-104">SYNTAX</span></span>

### <span data-ttu-id="f566f-105">S1</span><span class="sxs-lookup"><span data-stu-id="f566f-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f566f-106">S2</span><span class="sxs-lookup"><span data-stu-id="f566f-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f566f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f566f-107">DESCRIPTION</span></span>
<span data-ttu-id="f566f-108">Il cmdlet **Get-AzWebAppSlotPublishingProfile** ottiene il profilo di pubblicazione di Web App per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="f566f-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="f566f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f566f-109">EXAMPLES</span></span>

### <span data-ttu-id="f566f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f566f-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="f566f-111">Questo comando recupera il profilo di pubblicazione in formato Ftp per lo slot Slot001 relativo all'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="f566f-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="f566f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f566f-112">PARAMETERS</span></span>

### <span data-ttu-id="f566f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f566f-113">-DefaultProfile</span></span>
<span data-ttu-id="f566f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f566f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f566f-115">-Format</span><span class="sxs-lookup"><span data-stu-id="f566f-115">-Format</span></span>
<span data-ttu-id="f566f-116">Formato</span><span class="sxs-lookup"><span data-stu-id="f566f-116">Format</span></span>

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

### <span data-ttu-id="f566f-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="f566f-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="f566f-118">Includere gli endpoint di ripristino di emergenza, se vero</span><span class="sxs-lookup"><span data-stu-id="f566f-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="f566f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f566f-119">-Name</span></span>
<span data-ttu-id="f566f-120">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="f566f-120">WebApp Name</span></span>

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

### <span data-ttu-id="f566f-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="f566f-121">-OutputFile</span></span>
<span data-ttu-id="f566f-122">Output File</span><span class="sxs-lookup"><span data-stu-id="f566f-122">Output File</span></span>

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

### <span data-ttu-id="f566f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f566f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f566f-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f566f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f566f-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="f566f-125">-Slot</span></span>
<span data-ttu-id="f566f-126">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="f566f-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f566f-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f566f-127">-WebApp</span></span>
<span data-ttu-id="f566f-128">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="f566f-128">WebApp Object</span></span>

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

### <span data-ttu-id="f566f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f566f-129">CommonParameters</span></span>
<span data-ttu-id="f566f-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f566f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f566f-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f566f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f566f-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="f566f-132">INPUTS</span></span>

### <span data-ttu-id="f566f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f566f-133">System.String</span></span>

### <span data-ttu-id="f566f-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f566f-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f566f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f566f-135">OUTPUTS</span></span>

### <span data-ttu-id="f566f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f566f-136">System.String</span></span>

## <span data-ttu-id="f566f-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f566f-137">NOTES</span></span>

## <span data-ttu-id="f566f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f566f-138">RELATED LINKS</span></span>

[<span data-ttu-id="f566f-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f566f-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="f566f-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f566f-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="f566f-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f566f-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
