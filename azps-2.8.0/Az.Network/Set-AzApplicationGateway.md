---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 34f3de9e2dafe3cfb9b15aad1dda7d75bab67c20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854181"
---
# <span data-ttu-id="740fb-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="740fb-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="740fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="740fb-102">SYNOPSIS</span></span>
<span data-ttu-id="740fb-103">Aggiorna un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="740fb-103">Updates an application gateway.</span></span>

## <span data-ttu-id="740fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="740fb-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="740fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="740fb-105">DESCRIPTION</span></span>
<span data-ttu-id="740fb-106">Il cmdlet **set-AzApplicationGateway** aggiorna un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="740fb-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="740fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="740fb-107">EXAMPLES</span></span>

### <span data-ttu-id="740fb-108">Esempio 1: aggiornare un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="740fb-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="740fb-109">Questo comando Aggiorna il gateway dell'applicazione con le impostazioni nella variabile $AppGw e archivia il gateway aggiornato nella variabile $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="740fb-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="740fb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="740fb-110">PARAMETERS</span></span>

### <span data-ttu-id="740fb-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="740fb-111">-ApplicationGateway</span></span>
<span data-ttu-id="740fb-112">Specifica un oggetto gateway dell'applicazione che rappresenta lo stato in cui deve essere impostato il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="740fb-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="740fb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="740fb-113">-AsJob</span></span>
<span data-ttu-id="740fb-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="740fb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="740fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="740fb-115">-DefaultProfile</span></span>
<span data-ttu-id="740fb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="740fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="740fb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="740fb-117">CommonParameters</span></span>
<span data-ttu-id="740fb-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="740fb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="740fb-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="740fb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="740fb-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="740fb-120">INPUTS</span></span>

### <span data-ttu-id="740fb-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="740fb-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="740fb-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="740fb-122">OUTPUTS</span></span>

### <span data-ttu-id="740fb-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="740fb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="740fb-124">Note</span><span class="sxs-lookup"><span data-stu-id="740fb-124">NOTES</span></span>

## <span data-ttu-id="740fb-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="740fb-125">RELATED LINKS</span></span>

[<span data-ttu-id="740fb-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="740fb-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


