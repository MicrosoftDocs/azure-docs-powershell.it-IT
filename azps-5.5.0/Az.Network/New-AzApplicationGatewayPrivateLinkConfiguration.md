---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206843"
---
# <span data-ttu-id="978c2-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="978c2-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="978c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="978c2-102">SYNOPSIS</span></span>
<span data-ttu-id="978c2-103">Crea una configurazione di collegamento privato per un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="978c2-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="978c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="978c2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978c2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="978c2-105">DESCRIPTION</span></span>
<span data-ttu-id="978c2-106">Il cmdlet **New-AzApplicationGatewayPrivateLinkConfiguration** crea una configurazione PrivateLink per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="978c2-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="978c2-107">La configurazione dei collegamenti privati deve essere associata a una configurazione IP frontend per abilitare la funzionalità di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="978c2-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="978c2-108">Una configurazione di collegamento privato può essere associata a una sola configurazione IP frontend nel gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="978c2-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="978c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="978c2-109">EXAMPLES</span></span>

### <span data-ttu-id="978c2-110">Esempio 1: Creare una configurazione di collegamento privato con una singola configurazione IP</span><span class="sxs-lookup"><span data-stu-id="978c2-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="978c2-111">Questo comando crea una configurazione PrivateLink denominata 'privateLinkConfig01' e archivia il risultato nella variabile $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="978c2-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="978c2-112">Esempio 2: Creare una configurazione di collegamento privato con più configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="978c2-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="978c2-113">Questo comando crea una configurazione PrivateLink denominata 'privateLinkConfig01' con due ipConfigurations e archivia il risultato nella variabile $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="978c2-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="978c2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="978c2-114">PARAMETERS</span></span>

### <span data-ttu-id="978c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978c2-115">-DefaultProfile</span></span>
<span data-ttu-id="978c2-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="978c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978c2-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="978c2-117">-IpConfiguration</span></span>
<span data-ttu-id="978c2-118">Elenco di ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="978c2-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="978c2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="978c2-119">-Name</span></span>
<span data-ttu-id="978c2-120">Nome della configurazione privateLink</span><span class="sxs-lookup"><span data-stu-id="978c2-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="978c2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="978c2-121">-Confirm</span></span>
<span data-ttu-id="978c2-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978c2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978c2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978c2-123">-WhatIf</span></span>
<span data-ttu-id="978c2-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="978c2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="978c2-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="978c2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978c2-126">CommonParameters</span></span>
<span data-ttu-id="978c2-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978c2-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="978c2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978c2-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="978c2-129">INPUTS</span></span>

### <span data-ttu-id="978c2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="978c2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="978c2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="978c2-131">OUTPUTS</span></span>

### <span data-ttu-id="978c2-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="978c2-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="978c2-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="978c2-133">NOTES</span></span>

## <span data-ttu-id="978c2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="978c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="978c2-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="978c2-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="978c2-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="978c2-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="978c2-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="978c2-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="978c2-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="978c2-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
