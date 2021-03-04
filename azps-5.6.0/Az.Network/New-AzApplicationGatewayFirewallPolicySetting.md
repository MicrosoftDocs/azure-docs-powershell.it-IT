---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: 256509a42b844b196728b89b30abcdb6c5b9b386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962734"
---
# <span data-ttu-id="44836-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="44836-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="44836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44836-102">SYNOPSIS</span></span>
<span data-ttu-id="44836-103">Crea un'impostazione dei criteri per il criterio firewall</span><span class="sxs-lookup"><span data-stu-id="44836-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="44836-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44836-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44836-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="44836-105">DESCRIPTION</span></span>
<span data-ttu-id="44836-106">**New-AzApplicationGatewayFirewallPolicySetting** crea impostazioni dei criteri per un criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="44836-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="44836-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44836-107">EXAMPLES</span></span>

### <span data-ttu-id="44836-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44836-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="44836-109">Il comando crea un'impostazione del criterio con stato $enabledState, modalità come $enabledMode, RequestCheck come false, FileUploadLimitInMb come $fileUploadLimitInMb e MaxRequest UnaridimensionaInKb come $$maxRequestBodySizeInKb.</span><span class="sxs-lookup"><span data-stu-id="44836-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="44836-110">I nuovi criteri vengono archiviati in $condition.</span><span class="sxs-lookup"><span data-stu-id="44836-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="44836-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44836-111">PARAMETERS</span></span>

### <span data-ttu-id="44836-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44836-112">-DefaultProfile</span></span>
<span data-ttu-id="44836-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44836-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44836-114">-DisableRequestCheck</span><span class="sxs-lookup"><span data-stu-id="44836-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="44836-115">Diables the requestCheck in policy settings of the firewall policy.</span><span class="sxs-lookup"><span data-stu-id="44836-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="44836-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="44836-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="44836-117">Dimensioni massime di caricamento file in MB.</span><span class="sxs-lookup"><span data-stu-id="44836-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="44836-118">-MaxRequest UnaRidimensionaInKb</span><span class="sxs-lookup"><span data-stu-id="44836-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="44836-119">MaxRequestRequestSizeInKb nelle impostazioni dei criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="44836-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="44836-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="44836-120">-Mode</span></span>
<span data-ttu-id="44836-121">Modalità firewall nelle impostazioni dei criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="44836-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="44836-122">-State</span><span class="sxs-lookup"><span data-stu-id="44836-122">-State</span></span>
<span data-ttu-id="44836-123">Variabile di stato nelle impostazioni dei criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="44836-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="44836-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44836-124">CommonParameters</span></span>
<span data-ttu-id="44836-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44836-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44836-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44836-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44836-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="44836-127">INPUTS</span></span>

### <span data-ttu-id="44836-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="44836-128">None</span></span>

## <span data-ttu-id="44836-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44836-129">OUTPUTS</span></span>

### <span data-ttu-id="44836-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="44836-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="44836-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="44836-131">NOTES</span></span>

## <span data-ttu-id="44836-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44836-132">RELATED LINKS</span></span>
