---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192832"
---
# <span data-ttu-id="680e7-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="680e7-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="680e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="680e7-102">SYNOPSIS</span></span>
<span data-ttu-id="680e7-103">Crea una configurazione di collegamento privato per un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="680e7-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="680e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="680e7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="680e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="680e7-105">DESCRIPTION</span></span>
<span data-ttu-id="680e7-106">Il cmdlet **New-AzApplicationGatewayPrivateLinkConfiguration** crea una configurazione PrivateLink per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="680e7-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="680e7-107">La configurazione del collegamento privato deve essere associata a una configurazione IP di frontend per abilitare la funzionalità di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="680e7-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="680e7-108">La configurazione di un collegamento privato può essere associata a una sola configurazione IP del frontend nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="680e7-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="680e7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="680e7-109">EXAMPLES</span></span>

### <span data-ttu-id="680e7-110">Esempio 1: creare una configurazione di collegamento privato con la configurazione IP singola</span><span class="sxs-lookup"><span data-stu-id="680e7-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="680e7-111">Questo comando crea una configurazione PrivateLink denominata "privateLinkConfig01" e archivia il risultato nella variabile denominata $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="680e7-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="680e7-112">Esempio 2: creare una configurazione di collegamento privato con più configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="680e7-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="680e7-113">Questo comando crea una configurazione PrivateLink denominata "privateLinkConfig01" con due ipConfigurations e archivia il risultato nella variabile denominata $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="680e7-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="680e7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="680e7-114">PARAMETERS</span></span>

### <span data-ttu-id="680e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="680e7-115">-DefaultProfile</span></span>
<span data-ttu-id="680e7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="680e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="680e7-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="680e7-117">-IpConfiguration</span></span>
<span data-ttu-id="680e7-118">Elenco di ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="680e7-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="680e7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="680e7-119">-Name</span></span>
<span data-ttu-id="680e7-120">Nome della configurazione di privateLink</span><span class="sxs-lookup"><span data-stu-id="680e7-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="680e7-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="680e7-121">-Confirm</span></span>
<span data-ttu-id="680e7-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="680e7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="680e7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="680e7-123">-WhatIf</span></span>
<span data-ttu-id="680e7-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="680e7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="680e7-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="680e7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="680e7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="680e7-126">CommonParameters</span></span>
<span data-ttu-id="680e7-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="680e7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="680e7-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="680e7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="680e7-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="680e7-129">INPUTS</span></span>

### <span data-ttu-id="680e7-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="680e7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="680e7-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="680e7-131">OUTPUTS</span></span>

### <span data-ttu-id="680e7-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="680e7-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="680e7-133">Note</span><span class="sxs-lookup"><span data-stu-id="680e7-133">NOTES</span></span>

## <span data-ttu-id="680e7-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="680e7-134">RELATED LINKS</span></span>

[<span data-ttu-id="680e7-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="680e7-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="680e7-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="680e7-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="680e7-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="680e7-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="680e7-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="680e7-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)