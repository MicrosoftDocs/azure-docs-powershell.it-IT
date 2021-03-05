---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 5f63ee4d1c55211b13eb525a76547064e61cba48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001278"
---
# <span data-ttu-id="0fcbf-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="0fcbf-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="0fcbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fcbf-102">SYNOPSIS</span></span>
<span data-ttu-id="0fcbf-103">Creare un oggetto che rappresenti le impostazioni della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="0fcbf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fcbf-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fcbf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0fcbf-105">DESCRIPTION</span></span>
<span data-ttu-id="0fcbf-106">Creare un oggetto che rappresenti le impostazioni delle regole di rete che possono essere usate durante la creazione di un vault.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="0fcbf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fcbf-107">EXAMPLES</span></span>

### <span data-ttu-id="0fcbf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0fcbf-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="0fcbf-109">Creazione di un nuovo vault e specifica le regole di rete per consentire l'accesso all'indirizzo IP specificato dalla rete virtuale identificata $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="0fcbf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fcbf-110">PARAMETERS</span></span>

### <span data-ttu-id="0fcbf-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="0fcbf-111">-Bypass</span></span>
<span data-ttu-id="0fcbf-112">Specifica il bypass della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcbf-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="0fcbf-113">-DefaultAction</span></span>
<span data-ttu-id="0fcbf-114">Specifica l'azione predefinita della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcbf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fcbf-115">-DefaultProfile</span></span>
<span data-ttu-id="0fcbf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fcbf-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="0fcbf-117">-IpAddressRange</span></span>
<span data-ttu-id="0fcbf-118">Specifica l'intervallo di indirizzi IP di rete consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcbf-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0fcbf-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="0fcbf-120">Specifica l'identificatore di risorsa di rete virtuale consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcbf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fcbf-121">CommonParameters</span></span>
<span data-ttu-id="0fcbf-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fcbf-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0fcbf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fcbf-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="0fcbf-124">INPUTS</span></span>

### <span data-ttu-id="0fcbf-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0fcbf-125">None</span></span>

## <span data-ttu-id="0fcbf-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fcbf-126">OUTPUTS</span></span>

### <span data-ttu-id="0fcbf-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0fcbf-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="0fcbf-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="0fcbf-128">NOTES</span></span>

## <span data-ttu-id="0fcbf-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fcbf-129">RELATED LINKS</span></span>
