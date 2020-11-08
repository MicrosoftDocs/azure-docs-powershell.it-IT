---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193835"
---
# <span data-ttu-id="ec992-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="ec992-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="ec992-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec992-102">SYNOPSIS</span></span>
<span data-ttu-id="ec992-103">Ottenere le impostazioni di sicurezza in Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="ec992-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="ec992-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec992-104">SYNTAX</span></span>

### <span data-ttu-id="ec992-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec992-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec992-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ec992-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec992-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec992-107">DESCRIPTION</span></span>
<span data-ttu-id="ec992-108">Il cmdlet Get-AzSecuritySetting ottenere le impostazioni di sicurezza in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="ec992-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="ec992-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec992-109">EXAMPLES</span></span>

### <span data-ttu-id="ec992-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ec992-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="ec992-111">Ottiene un'impostazione di esportazione dei dati di MCAS</span><span class="sxs-lookup"><span data-stu-id="ec992-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="ec992-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec992-112">PARAMETERS</span></span>

### <span data-ttu-id="ec992-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec992-113">-DefaultProfile</span></span>
<span data-ttu-id="ec992-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec992-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec992-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="ec992-115">-SettingName</span></span>
<span data-ttu-id="ec992-116">Impostazione del nome.</span><span class="sxs-lookup"><span data-stu-id="ec992-116">Setting name.</span></span> <span data-ttu-id="ec992-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="ec992-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="ec992-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec992-118">CommonParameters</span></span>
<span data-ttu-id="ec992-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec992-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec992-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec992-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec992-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec992-121">INPUTS</span></span>

### <span data-ttu-id="ec992-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ec992-122">System.String</span></span>

## <span data-ttu-id="ec992-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec992-123">OUTPUTS</span></span>

### <span data-ttu-id="ec992-124">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="ec992-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="ec992-125">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="ec992-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="ec992-126">Note</span><span class="sxs-lookup"><span data-stu-id="ec992-126">NOTES</span></span>

## <span data-ttu-id="ec992-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec992-127">RELATED LINKS</span></span>