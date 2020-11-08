---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: 378c6ee91c438bfa70ab8e89e069ad81d3515e33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032963"
---
# <span data-ttu-id="29c11-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="29c11-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="29c11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29c11-102">SYNOPSIS</span></span>
<span data-ttu-id="29c11-103">Ottiene l'integrità del backend di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="29c11-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="29c11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29c11-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29c11-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29c11-105">DESCRIPTION</span></span>
<span data-ttu-id="29c11-106">Il cmdlet Get-AzApplicationGatewayBackendHealth Ottiene l'integrità del backend di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="29c11-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="29c11-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29c11-107">EXAMPLES</span></span>

### <span data-ttu-id="29c11-108">Esempio 1: Ottiene l'integrità del backend senza risorse espanse.</span><span class="sxs-lookup"><span data-stu-id="29c11-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="29c11-109">Questo comando consente di ottenere lo stato di integrità del gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="29c11-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="29c11-110">Esempio 2: Ottiene l'integrità del backend con risorse espanse.</span><span class="sxs-lookup"><span data-stu-id="29c11-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="29c11-111">Questo comando consente di ottenere lo stato di back-end (con risorse espanse) del gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="29c11-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="29c11-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29c11-112">PARAMETERS</span></span>

### <span data-ttu-id="29c11-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29c11-113">-AsJob</span></span>
<span data-ttu-id="29c11-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="29c11-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29c11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c11-115">-DefaultProfile</span></span>
<span data-ttu-id="29c11-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29c11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29c11-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="29c11-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29c11-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="29c11-118">-Name</span></span>
<span data-ttu-id="29c11-119">Specifica il nome del gateway dell'applicazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29c11-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29c11-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c11-120">-ResourceGroupName</span></span>
<span data-ttu-id="29c11-121">Specifica il nome del gruppo di risorse che contiene il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="29c11-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29c11-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c11-122">CommonParameters</span></span>
<span data-ttu-id="29c11-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c11-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c11-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29c11-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c11-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29c11-125">INPUTS</span></span>

### <span data-ttu-id="29c11-126">System. String</span><span class="sxs-lookup"><span data-stu-id="29c11-126">System.String</span></span>

## <span data-ttu-id="29c11-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29c11-127">OUTPUTS</span></span>

### <span data-ttu-id="29c11-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="29c11-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="29c11-129">Note</span><span class="sxs-lookup"><span data-stu-id="29c11-129">NOTES</span></span>
<span data-ttu-id="29c11-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="29c11-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="29c11-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29c11-131">RELATED LINKS</span></span>

[<span data-ttu-id="29c11-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="29c11-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

