---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: ca59a1b2e156bc23b082a8307eb034b13b78105e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003533"
---
# <span data-ttu-id="32f25-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32f25-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="32f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32f25-102">SYNOPSIS</span></span>
<span data-ttu-id="32f25-103">Aggiorna un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="32f25-103">Updates an application gateway.</span></span>

## <span data-ttu-id="32f25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32f25-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32f25-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32f25-105">DESCRIPTION</span></span>
<span data-ttu-id="32f25-106">Il cmdlet **Set-AzApplicationGateway** aggiorna un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="32f25-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="32f25-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32f25-107">EXAMPLES</span></span>

### <span data-ttu-id="32f25-108">Esempio 1: Aggiornare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="32f25-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="32f25-109">Questi comandi aggiornano il gateway applicazione con le impostazioni nella variabile $AppGw e archiviano il gateway aggiornato nella variabile $UpdatedAppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="32f25-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="32f25-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32f25-110">PARAMETERS</span></span>

### <span data-ttu-id="32f25-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32f25-111">-ApplicationGateway</span></span>
<span data-ttu-id="32f25-112">Specifica un oggetto gateway applicazione che rappresenta lo stato su cui deve essere impostato il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="32f25-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32f25-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32f25-113">-AsJob</span></span>
<span data-ttu-id="32f25-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="32f25-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32f25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32f25-115">-DefaultProfile</span></span>
<span data-ttu-id="32f25-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32f25-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32f25-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f25-117">CommonParameters</span></span>
<span data-ttu-id="32f25-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32f25-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f25-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32f25-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f25-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="32f25-120">INPUTS</span></span>

### <span data-ttu-id="32f25-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32f25-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="32f25-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32f25-122">OUTPUTS</span></span>

### <span data-ttu-id="32f25-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32f25-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="32f25-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="32f25-124">NOTES</span></span>

## <span data-ttu-id="32f25-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32f25-125">RELATED LINKS</span></span>

[<span data-ttu-id="32f25-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32f25-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


