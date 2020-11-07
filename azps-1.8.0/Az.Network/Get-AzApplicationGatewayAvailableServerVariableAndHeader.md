---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8f0fc8caba03251ede507fc383ef99c10a06eeb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678627"
---
# <span data-ttu-id="8b9c8-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="8b9c8-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="8b9c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b9c8-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9c8-103">Ottenere le variabili server supportate e le intestazioni di richiesta e risposta disponibili.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="8b9c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b9c8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="8b9c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b9c8-105">DESCRIPTION</span></span>
<span data-ttu-id="8b9c8-106">Il cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** ottiene le variabili server supportate e le intestazioni di richiesta e risposta disponibili.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="8b9c8-107">I parametri possono essere usati per ottenere le variabili o gli elenchi di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="8b9c8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b9c8-108">EXAMPLES</span></span>

### <span data-ttu-id="8b9c8-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b9c8-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="8b9c8-110">Questi comandi restituiscono tutte le variabili del server disponibili.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="8b9c8-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8b9c8-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="8b9c8-112">Questi comandi restituiscono tutte le intestazioni di richiesta disponibili.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="8b9c8-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8b9c8-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="8b9c8-114">Questi comandi restituiscono tutte le intestazioni di risposta disponibili.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="8b9c8-115">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="8b9c8-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="8b9c8-116">Questi comandi restituiscono tutte le variabili server disponibili, le intestazioni di richiesta e risposta.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="8b9c8-117">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="8b9c8-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="8b9c8-118">Questi comandi restituiscono tutte le variabili server disponibili, le intestazioni di richiesta e risposta.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="8b9c8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b9c8-119">PARAMETERS</span></span>

### <span data-ttu-id="8b9c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9c8-120">-DefaultProfile</span></span>
<span data-ttu-id="8b9c8-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b9c8-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="8b9c8-122">-RequestHeader</span></span>
<span data-ttu-id="8b9c8-123">Intestazioni delle richieste disponibili per Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="8b9c8-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="8b9c8-124">-ResponseHeader</span></span>
<span data-ttu-id="8b9c8-125">Intestazioni di risposta disponibili in Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="8b9c8-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="8b9c8-126">-ServerVariable</span></span>
<span data-ttu-id="8b9c8-127">Variabili server disponibili in Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="8b9c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9c8-128">CommonParameters</span></span>
<span data-ttu-id="8b9c8-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b9c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9c8-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b9c8-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9c8-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b9c8-131">INPUTS</span></span>

### <span data-ttu-id="8b9c8-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8b9c8-132">None</span></span>

## <span data-ttu-id="8b9c8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b9c8-133">OUTPUTS</span></span>

### <span data-ttu-id="8b9c8-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="8b9c8-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="8b9c8-135">Note</span><span class="sxs-lookup"><span data-stu-id="8b9c8-135">NOTES</span></span>
<span data-ttu-id="8b9c8-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .</span><span class="sxs-lookup"><span data-stu-id="8b9c8-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="8b9c8-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b9c8-137">RELATED LINKS</span></span>
