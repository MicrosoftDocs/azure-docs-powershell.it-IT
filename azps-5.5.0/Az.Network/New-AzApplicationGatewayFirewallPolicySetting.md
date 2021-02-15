---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193702"
---
# <span data-ttu-id="cab45-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="cab45-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="cab45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab45-102">SYNOPSIS</span></span>
<span data-ttu-id="cab45-103">Crea un'impostazione dei criteri per il criterio firewall</span><span class="sxs-lookup"><span data-stu-id="cab45-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="cab45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cab45-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cab45-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cab45-105">DESCRIPTION</span></span>
<span data-ttu-id="cab45-106">**New-AzApplicationGatewayFirewallPolicySetting** crea impostazioni dei criteri per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="cab45-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="cab45-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cab45-107">EXAMPLES</span></span>

### <span data-ttu-id="cab45-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cab45-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="cab45-109">Il comando crea un'impostazione di criteri con stato $enabledState, modalità come $enabledMode, RequestCheck come false, FileUploadLimitInMb come $fileUploadLimitInMb e MaxRequest UnaridimensionaInKb come $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="cab45-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="cab45-110">Il nuovo policySettings viene archiviato in $condition.</span><span class="sxs-lookup"><span data-stu-id="cab45-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="cab45-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cab45-111">PARAMETERS</span></span>

### <span data-ttu-id="cab45-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab45-112">-DefaultProfile</span></span>
<span data-ttu-id="cab45-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cab45-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab45-114">-DisableRequestCheck</span><span class="sxs-lookup"><span data-stu-id="cab45-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="cab45-115">Diables the requestCheck in policy settings of the firewall policy.</span><span class="sxs-lookup"><span data-stu-id="cab45-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="cab45-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="cab45-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="cab45-117">Dimensioni massime di caricamento file in MB.</span><span class="sxs-lookup"><span data-stu-id="cab45-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="cab45-118">-MaxRequest UnaRidimensionaInKb</span><span class="sxs-lookup"><span data-stu-id="cab45-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="cab45-119">MaxRequestRequestSizeInKb nelle impostazioni dei criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="cab45-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="cab45-120">-Modalità</span><span class="sxs-lookup"><span data-stu-id="cab45-120">-Mode</span></span>
<span data-ttu-id="cab45-121">Modalità firewall nelle impostazioni dei criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="cab45-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="cab45-122">-State</span><span class="sxs-lookup"><span data-stu-id="cab45-122">-State</span></span>
<span data-ttu-id="cab45-123">Variabile di stato nelle impostazioni dei criteri del criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="cab45-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="cab45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab45-124">CommonParameters</span></span>
<span data-ttu-id="cab45-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab45-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cab45-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab45-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="cab45-127">INPUTS</span></span>

### <span data-ttu-id="cab45-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cab45-128">None</span></span>

## <span data-ttu-id="cab45-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cab45-129">OUTPUTS</span></span>

### <span data-ttu-id="cab45-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="cab45-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="cab45-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="cab45-131">NOTES</span></span>

## <span data-ttu-id="cab45-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cab45-132">RELATED LINKS</span></span>
