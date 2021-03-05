---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 00df9069400a1d3e2ae10abfb03d9d55bff08735
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972366"
---
# <span data-ttu-id="ba5a8-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba5a8-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ba5a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba5a8-102">SYNOPSIS</span></span>

## <span data-ttu-id="ba5a8-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba5a8-103">SYNTAX</span></span>

### <span data-ttu-id="ba5a8-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ba5a8-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba5a8-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ba5a8-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba5a8-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba5a8-106">DESCRIPTION</span></span>
<span data-ttu-id="ba5a8-107">Il **cmdlet Get-AzWebAppBackupConfiguration** ottiene la configurazione di backup di un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="ba5a8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba5a8-108">EXAMPLES</span></span>

### <span data-ttu-id="ba5a8-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ba5a8-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="ba5a8-110">Questo comando recupera la configurazione di backup dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ba5a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba5a8-111">PARAMETERS</span></span>

### <span data-ttu-id="ba5a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5a8-112">-DefaultProfile</span></span>
<span data-ttu-id="ba5a8-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba5a8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ba5a8-114">-Name</span></span>
<span data-ttu-id="ba5a8-115">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="ba5a8-115">WebApp Name</span></span>

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

### <span data-ttu-id="ba5a8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba5a8-116">-ResourceGroupName</span></span>
<span data-ttu-id="ba5a8-117">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ba5a8-117">Resource Group Name</span></span>

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

### <span data-ttu-id="ba5a8-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="ba5a8-118">-Slot</span></span>
<span data-ttu-id="ba5a8-119">Nome slot</span><span class="sxs-lookup"><span data-stu-id="ba5a8-119">Slot Name</span></span>

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

### <span data-ttu-id="ba5a8-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ba5a8-120">-WebApp</span></span>
<span data-ttu-id="ba5a8-121">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="ba5a8-121">WebApp Name</span></span>

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

### <span data-ttu-id="ba5a8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5a8-122">CommonParameters</span></span>
<span data-ttu-id="ba5a8-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba5a8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5a8-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5a8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5a8-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba5a8-125">INPUTS</span></span>

### <span data-ttu-id="ba5a8-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ba5a8-126">System.String</span></span>

### <span data-ttu-id="ba5a8-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ba5a8-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ba5a8-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba5a8-128">OUTPUTS</span></span>

### <span data-ttu-id="ba5a8-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba5a8-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ba5a8-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba5a8-130">NOTES</span></span>

## <span data-ttu-id="ba5a8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba5a8-131">RELATED LINKS</span></span>
