---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 38a9d9d36d4abdf85149fe9d7da5387468985daf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347932"
---
# <span data-ttu-id="e372e-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e372e-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="e372e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e372e-102">SYNOPSIS</span></span>
<span data-ttu-id="e372e-103">Aggiorna un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e372e-103">Updates an application gateway.</span></span>

## <span data-ttu-id="e372e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e372e-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e372e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e372e-105">DESCRIPTION</span></span>
<span data-ttu-id="e372e-106">Il cmdlet **set-AzApplicationGateway** aggiorna un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="e372e-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="e372e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e372e-107">EXAMPLES</span></span>

### <span data-ttu-id="e372e-108">Esempio 1: aggiornare un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="e372e-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e372e-109">Questi comandi aggiornano il gateway dell'applicazione con le impostazioni nella variabile $AppGw e archiviano il gateway aggiornato nella variabile $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="e372e-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="e372e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e372e-110">PARAMETERS</span></span>

### <span data-ttu-id="e372e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e372e-111">-ApplicationGateway</span></span>
<span data-ttu-id="e372e-112">Specifica un oggetto gateway dell'applicazione che rappresenta lo stato in cui deve essere impostato il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e372e-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="e372e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e372e-113">-AsJob</span></span>
<span data-ttu-id="e372e-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e372e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e372e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e372e-115">-DefaultProfile</span></span>
<span data-ttu-id="e372e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e372e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e372e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e372e-117">CommonParameters</span></span>
<span data-ttu-id="e372e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e372e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e372e-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e372e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e372e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e372e-120">INPUTS</span></span>

### <span data-ttu-id="e372e-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e372e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e372e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e372e-122">OUTPUTS</span></span>

### <span data-ttu-id="e372e-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e372e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e372e-124">Note</span><span class="sxs-lookup"><span data-stu-id="e372e-124">NOTES</span></span>

## <span data-ttu-id="e372e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e372e-125">RELATED LINKS</span></span>

[<span data-ttu-id="e372e-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e372e-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


