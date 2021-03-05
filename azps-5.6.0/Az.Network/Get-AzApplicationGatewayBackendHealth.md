---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: b5910352c8abcfb880a1007a3f2246ff7c12d9f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003614"
---
# <span data-ttu-id="34728-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="34728-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="34728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34728-102">SYNOPSIS</span></span>
<span data-ttu-id="34728-103">Recupera l'integrità back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="34728-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="34728-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34728-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34728-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34728-105">DESCRIPTION</span></span>
<span data-ttu-id="34728-106">Il cmdlet Get-AzApplicationGatewayBackendHealth recupera l'integrità back-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="34728-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="34728-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34728-107">EXAMPLES</span></span>

### <span data-ttu-id="34728-108">Esempio 1: recupera l'integrità del back-end senza risorse espanse.</span><span class="sxs-lookup"><span data-stu-id="34728-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="34728-109">Questo comando recupera l'integrità back-end del gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $BackendHealth variabile.</span><span class="sxs-lookup"><span data-stu-id="34728-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="34728-110">Esempio 2: Recupera l'integrità back-end con risorse espanse.</span><span class="sxs-lookup"><span data-stu-id="34728-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="34728-111">Questo comando recupera l'integrità back-end (con risorse espanse) del gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $BackendHealth variabile.</span><span class="sxs-lookup"><span data-stu-id="34728-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="34728-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34728-112">PARAMETERS</span></span>

### <span data-ttu-id="34728-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34728-113">-AsJob</span></span>
<span data-ttu-id="34728-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="34728-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34728-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34728-115">-DefaultProfile</span></span>
<span data-ttu-id="34728-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34728-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34728-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="34728-117">-ExpandResource</span></span>
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

### <span data-ttu-id="34728-118">-Name</span><span class="sxs-lookup"><span data-stu-id="34728-118">-Name</span></span>
<span data-ttu-id="34728-119">Specifica il nome del gateway applicazione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34728-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="34728-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34728-120">-ResourceGroupName</span></span>
<span data-ttu-id="34728-121">Specifica il nome del gruppo di risorse che contiene il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="34728-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="34728-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34728-122">CommonParameters</span></span>
<span data-ttu-id="34728-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34728-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34728-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34728-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34728-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="34728-125">INPUTS</span></span>

### <span data-ttu-id="34728-126">System.String</span><span class="sxs-lookup"><span data-stu-id="34728-126">System.String</span></span>

## <span data-ttu-id="34728-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34728-127">OUTPUTS</span></span>

### <span data-ttu-id="34728-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="34728-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="34728-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="34728-129">NOTES</span></span>
<span data-ttu-id="34728-130">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="34728-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="34728-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34728-131">RELATED LINKS</span></span>

[<span data-ttu-id="34728-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34728-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

