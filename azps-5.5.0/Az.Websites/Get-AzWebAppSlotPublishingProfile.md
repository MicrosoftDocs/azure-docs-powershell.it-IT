---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195494"
---
# <span data-ttu-id="b76b3-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b76b3-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="b76b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b76b3-102">SYNOPSIS</span></span>
<span data-ttu-id="b76b3-103">Ottiene un profilo di pubblicazione degli slot per Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b76b3-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="b76b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b76b3-104">SYNTAX</span></span>

### <span data-ttu-id="b76b3-105">S1</span><span class="sxs-lookup"><span data-stu-id="b76b3-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b76b3-106">S2</span><span class="sxs-lookup"><span data-stu-id="b76b3-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b76b3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b76b3-107">DESCRIPTION</span></span>
<span data-ttu-id="b76b3-108">Il cmdlet **Get-AzWebAppSlotPublishingProfile** ottiene il profilo di pubblicazione di Web App per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="b76b3-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="b76b3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b76b3-109">EXAMPLES</span></span>

### <span data-ttu-id="b76b3-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b76b3-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="b76b3-111">Questo comando recupera il profilo di pubblicazione in formato Ftp per lo slot Slot001 relativo all'app Web ContosoWebApp associata al gruppo di risorse Default-Web-WestUS e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="b76b3-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="b76b3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b76b3-112">PARAMETERS</span></span>

### <span data-ttu-id="b76b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76b3-113">-DefaultProfile</span></span>
<span data-ttu-id="b76b3-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b76b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76b3-115">-Format</span><span class="sxs-lookup"><span data-stu-id="b76b3-115">-Format</span></span>
<span data-ttu-id="b76b3-116">Formato</span><span class="sxs-lookup"><span data-stu-id="b76b3-116">Format</span></span>

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

### <span data-ttu-id="b76b3-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="b76b3-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="b76b3-118">Includere gli endpoint di ripristino di emergenza, se vero</span><span class="sxs-lookup"><span data-stu-id="b76b3-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="b76b3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b76b3-119">-Name</span></span>
<span data-ttu-id="b76b3-120">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="b76b3-120">WebApp Name</span></span>

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

### <span data-ttu-id="b76b3-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="b76b3-121">-OutputFile</span></span>
<span data-ttu-id="b76b3-122">Output File</span><span class="sxs-lookup"><span data-stu-id="b76b3-122">Output File</span></span>

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

### <span data-ttu-id="b76b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="b76b3-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b76b3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b76b3-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="b76b3-125">-Slot</span></span>
<span data-ttu-id="b76b3-126">Nome slot WebApp</span><span class="sxs-lookup"><span data-stu-id="b76b3-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b76b3-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b76b3-127">-WebApp</span></span>
<span data-ttu-id="b76b3-128">Oggetto WebApp</span><span class="sxs-lookup"><span data-stu-id="b76b3-128">WebApp Object</span></span>

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

### <span data-ttu-id="b76b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76b3-129">CommonParameters</span></span>
<span data-ttu-id="b76b3-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76b3-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76b3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76b3-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b76b3-132">INPUTS</span></span>

### <span data-ttu-id="b76b3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b76b3-133">System.String</span></span>

### <span data-ttu-id="b76b3-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b76b3-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b76b3-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b76b3-135">OUTPUTS</span></span>

### <span data-ttu-id="b76b3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b76b3-136">System.String</span></span>

## <span data-ttu-id="b76b3-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="b76b3-137">NOTES</span></span>

## <span data-ttu-id="b76b3-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b76b3-138">RELATED LINKS</span></span>

[<span data-ttu-id="b76b3-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="b76b3-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="b76b3-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b76b3-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b76b3-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b76b3-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
