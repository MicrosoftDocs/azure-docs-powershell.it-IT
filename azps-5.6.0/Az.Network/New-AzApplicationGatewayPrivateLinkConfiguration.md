---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 7c338f49191071bfa48214e65f79e196a75650eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973678"
---
# <span data-ttu-id="731a0-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="731a0-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="731a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="731a0-102">SYNOPSIS</span></span>
<span data-ttu-id="731a0-103">Crea una configurazione di collegamento privato per un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="731a0-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="731a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="731a0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="731a0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="731a0-105">DESCRIPTION</span></span>
<span data-ttu-id="731a0-106">Il cmdlet **New-AzApplicationGatewayPrivateLinkConfiguration** crea una configurazione PrivateLink per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="731a0-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="731a0-107">La configurazione dei collegamenti privati deve essere associata a una configurazione IP frontend per abilitare la funzionalità di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="731a0-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="731a0-108">Una configurazione di collegamento privato può essere associata a una sola configurazione IP frontend nel gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="731a0-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="731a0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="731a0-109">EXAMPLES</span></span>

### <span data-ttu-id="731a0-110">Esempio 1: Creare una configurazione di collegamento privato con una singola configurazione IP</span><span class="sxs-lookup"><span data-stu-id="731a0-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="731a0-111">Questo comando crea una configurazione PrivateLink denominata 'privateLinkConfig01' e archivia il risultato nella variabile $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="731a0-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="731a0-112">Esempio 2: Creare una configurazione di collegamento privato con più configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="731a0-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="731a0-113">Questo comando crea una configurazione PrivateLink denominata 'privateLinkConfig01' con due ipConfigurations e archivia il risultato nella variabile $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="731a0-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="731a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="731a0-114">PARAMETERS</span></span>

### <span data-ttu-id="731a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="731a0-115">-DefaultProfile</span></span>
<span data-ttu-id="731a0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="731a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="731a0-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="731a0-117">-IpConfiguration</span></span>
<span data-ttu-id="731a0-118">Elenco di ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="731a0-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="731a0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="731a0-119">-Name</span></span>
<span data-ttu-id="731a0-120">Nome della configurazione privateLink</span><span class="sxs-lookup"><span data-stu-id="731a0-120">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731a0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="731a0-121">-Confirm</span></span>
<span data-ttu-id="731a0-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="731a0-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731a0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="731a0-123">-WhatIf</span></span>
<span data-ttu-id="731a0-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="731a0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="731a0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="731a0-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="731a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="731a0-126">CommonParameters</span></span>
<span data-ttu-id="731a0-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="731a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="731a0-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="731a0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="731a0-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="731a0-129">INPUTS</span></span>

### <span data-ttu-id="731a0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="731a0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="731a0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="731a0-131">OUTPUTS</span></span>

### <span data-ttu-id="731a0-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="731a0-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="731a0-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="731a0-133">NOTES</span></span>

## <span data-ttu-id="731a0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="731a0-134">RELATED LINKS</span></span>

[<span data-ttu-id="731a0-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="731a0-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="731a0-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="731a0-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="731a0-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="731a0-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="731a0-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="731a0-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
