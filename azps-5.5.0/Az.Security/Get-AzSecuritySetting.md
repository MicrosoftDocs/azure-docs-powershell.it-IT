---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189135"
---
# <span data-ttu-id="d7560-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="d7560-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="d7560-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7560-102">SYNOPSIS</span></span>
<span data-ttu-id="d7560-103">Ottenere le impostazioni di sicurezza nel Centro sicurezza di Azure</span><span class="sxs-lookup"><span data-stu-id="d7560-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="d7560-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7560-104">SYNTAX</span></span>

### <span data-ttu-id="d7560-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7560-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7560-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d7560-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7560-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7560-107">DESCRIPTION</span></span>
<span data-ttu-id="d7560-108">Il cmdlet Get-AzSecuritySetting ottenere le impostazioni di sicurezza nel Centro sicurezza di Azure.</span><span class="sxs-lookup"><span data-stu-id="d7560-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="d7560-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7560-109">EXAMPLES</span></span>

### <span data-ttu-id="d7560-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d7560-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="d7560-111">Ottiene un'impostazione di esportazione dati MCAS</span><span class="sxs-lookup"><span data-stu-id="d7560-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="d7560-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7560-112">PARAMETERS</span></span>

### <span data-ttu-id="d7560-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7560-113">-DefaultProfile</span></span>
<span data-ttu-id="d7560-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7560-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7560-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="d7560-115">-SettingName</span></span>
<span data-ttu-id="d7560-116">Nome dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="d7560-116">Setting name.</span></span> <span data-ttu-id="d7560-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="d7560-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="d7560-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7560-118">CommonParameters</span></span>
<span data-ttu-id="d7560-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7560-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7560-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7560-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7560-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7560-121">INPUTS</span></span>

### <span data-ttu-id="d7560-122">System.String</span><span class="sxs-lookup"><span data-stu-id="d7560-122">System.String</span></span>

## <span data-ttu-id="d7560-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7560-123">OUTPUTS</span></span>

### <span data-ttu-id="d7560-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="d7560-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="d7560-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="d7560-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="d7560-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7560-126">NOTES</span></span>

## <span data-ttu-id="d7560-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7560-127">RELATED LINKS</span></span>
