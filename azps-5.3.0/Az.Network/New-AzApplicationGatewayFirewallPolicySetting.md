---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385601"
---
# <span data-ttu-id="22930-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="22930-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="22930-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22930-102">SYNOPSIS</span></span>
<span data-ttu-id="22930-103">Crea un'impostazione di criteri per il criterio firewall</span><span class="sxs-lookup"><span data-stu-id="22930-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="22930-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22930-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22930-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22930-105">DESCRIPTION</span></span>
<span data-ttu-id="22930-106">Il **nuovo AzApplicationGatewayFirewallPolicySetting** crea una delle impostazioni dei criteri per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="22930-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="22930-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22930-107">EXAMPLES</span></span>

### <span data-ttu-id="22930-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22930-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="22930-109">Il comando crea un'impostazione di criteri con lo stato come $enabledState, modalità come $enabledMode, RequestBodyCheck come false, FileUploadLimitInMb come $fileUploadLimitInMb e MaxRequestBodySizeInKb come $ $maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="22930-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="22930-110">La nuova policySettings è archiviata in $condition.</span><span class="sxs-lookup"><span data-stu-id="22930-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="22930-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22930-111">PARAMETERS</span></span>

### <span data-ttu-id="22930-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22930-112">-DefaultProfile</span></span>
<span data-ttu-id="22930-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22930-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22930-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="22930-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="22930-115">Disabilita il requestBodyCheck nelle impostazioni dei criteri del criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="22930-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="22930-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="22930-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="22930-117">Dimensioni massime FileUpload in MB.</span><span class="sxs-lookup"><span data-stu-id="22930-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22930-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="22930-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="22930-119">MaxRequestBodySizeInKb in impostazioni dei criteri del criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="22930-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22930-120">-Modalità</span><span class="sxs-lookup"><span data-stu-id="22930-120">-Mode</span></span>
<span data-ttu-id="22930-121">Modalità firewall in impostazioni dei criteri del criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="22930-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22930-122">-Stato</span><span class="sxs-lookup"><span data-stu-id="22930-122">-State</span></span>
<span data-ttu-id="22930-123">Variabile di stato nelle impostazioni dei criteri del criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="22930-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22930-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22930-124">CommonParameters</span></span>
<span data-ttu-id="22930-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22930-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22930-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22930-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22930-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22930-127">INPUTS</span></span>

### <span data-ttu-id="22930-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22930-128">None</span></span>

## <span data-ttu-id="22930-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22930-129">OUTPUTS</span></span>

### <span data-ttu-id="22930-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="22930-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="22930-131">Note</span><span class="sxs-lookup"><span data-stu-id="22930-131">NOTES</span></span>

## <span data-ttu-id="22930-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22930-132">RELATED LINKS</span></span>
