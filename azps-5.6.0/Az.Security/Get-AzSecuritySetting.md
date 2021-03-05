---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 7c443625294b3a23ac79dfcbabb724a2d3fceaa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971742"
---
# <span data-ttu-id="36be7-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="36be7-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="36be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36be7-102">SYNOPSIS</span></span>
<span data-ttu-id="36be7-103">Ottenere le impostazioni di sicurezza nel Centro sicurezza di Azure</span><span class="sxs-lookup"><span data-stu-id="36be7-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="36be7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36be7-104">SYNTAX</span></span>

### <span data-ttu-id="36be7-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36be7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36be7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="36be7-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36be7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36be7-107">DESCRIPTION</span></span>
<span data-ttu-id="36be7-108">Il cmdlet Get-AzSecuritySetting ottenere le impostazioni di sicurezza nel Centro sicurezza di Azure.</span><span class="sxs-lookup"><span data-stu-id="36be7-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="36be7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36be7-109">EXAMPLES</span></span>

### <span data-ttu-id="36be7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36be7-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="36be7-111">Ottiene un'impostazione di esportazione dati MCAS</span><span class="sxs-lookup"><span data-stu-id="36be7-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="36be7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36be7-112">PARAMETERS</span></span>

### <span data-ttu-id="36be7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36be7-113">-DefaultProfile</span></span>
<span data-ttu-id="36be7-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36be7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36be7-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="36be7-115">-SettingName</span></span>
<span data-ttu-id="36be7-116">Nome dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="36be7-116">Setting name.</span></span> <span data-ttu-id="36be7-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="36be7-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36be7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36be7-118">CommonParameters</span></span>
<span data-ttu-id="36be7-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36be7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36be7-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36be7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36be7-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="36be7-121">INPUTS</span></span>

### <span data-ttu-id="36be7-122">System.String</span><span class="sxs-lookup"><span data-stu-id="36be7-122">System.String</span></span>

## <span data-ttu-id="36be7-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36be7-123">OUTPUTS</span></span>

### <span data-ttu-id="36be7-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="36be7-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="36be7-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="36be7-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="36be7-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="36be7-126">NOTES</span></span>

## <span data-ttu-id="36be7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36be7-127">RELATED LINKS</span></span>
