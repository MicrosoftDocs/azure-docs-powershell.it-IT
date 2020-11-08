---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189687"
---
# <span data-ttu-id="fd646-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="fd646-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="fd646-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd646-102">SYNOPSIS</span></span>
<span data-ttu-id="fd646-103">Creare un oggetto che rappresenta le impostazioni della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="fd646-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="fd646-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd646-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd646-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd646-105">DESCRIPTION</span></span>
<span data-ttu-id="fd646-106">Crea un oggetto che rappresenta le impostazioni della regola di rete che possono essere usate per la creazione di un Vault.</span><span class="sxs-lookup"><span data-stu-id="fd646-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="fd646-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd646-107">EXAMPLES</span></span>

### <span data-ttu-id="fd646-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd646-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="fd646-109">Creare un nuovo Vault e specificare le regole di rete per consentire l'accesso all'indirizzo IP specificato dalla rete virtuale identificata da $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="fd646-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="fd646-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd646-110">PARAMETERS</span></span>

### <span data-ttu-id="fd646-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="fd646-111">-Bypass</span></span>
<span data-ttu-id="fd646-112">Specifica l'esclusione della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="fd646-112">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="fd646-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="fd646-113">-DefaultAction</span></span>
<span data-ttu-id="fd646-114">Specifica l'azione predefinita della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="fd646-114">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="fd646-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd646-115">-DefaultProfile</span></span>
<span data-ttu-id="fd646-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd646-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd646-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="fd646-117">-IpAddressRange</span></span>
<span data-ttu-id="fd646-118">Specifica l'intervallo di indirizzi IP di rete consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="fd646-118">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="fd646-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="fd646-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="fd646-120">Specifica l'identificatore delle risorse di rete virtuale consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="fd646-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="fd646-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd646-121">CommonParameters</span></span>
<span data-ttu-id="fd646-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd646-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd646-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd646-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd646-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd646-124">INPUTS</span></span>

### <span data-ttu-id="fd646-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fd646-125">None</span></span>

## <span data-ttu-id="fd646-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd646-126">OUTPUTS</span></span>

### <span data-ttu-id="fd646-127">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="fd646-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="fd646-128">Note</span><span class="sxs-lookup"><span data-stu-id="fd646-128">NOTES</span></span>

## <span data-ttu-id="fd646-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd646-129">RELATED LINKS</span></span>
