---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475537"
---
# <span data-ttu-id="edc44-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="edc44-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="edc44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="edc44-102">SYNOPSIS</span></span>
<span data-ttu-id="edc44-103">Ottenere le variabili server supportate e le intestazioni di richiesta e risposta disponibili.</span><span class="sxs-lookup"><span data-stu-id="edc44-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="edc44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="edc44-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="edc44-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edc44-105">DESCRIPTION</span></span>
<span data-ttu-id="edc44-106">Il cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** ottiene le variabili server supportate e le intestazioni di richiesta e risposta disponibili.</span><span class="sxs-lookup"><span data-stu-id="edc44-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="edc44-107">I parametri possono essere usati per ottenere le variabili o gli elenchi di intestazioni.</span><span class="sxs-lookup"><span data-stu-id="edc44-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="edc44-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="edc44-108">EXAMPLES</span></span>

### <span data-ttu-id="edc44-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="edc44-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="edc44-110">Questi comandi restituiscono tutte le variabili del server disponibili.</span><span class="sxs-lookup"><span data-stu-id="edc44-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="edc44-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="edc44-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="edc44-112">Questi comandi restituiscono tutte le intestazioni di richiesta disponibili.</span><span class="sxs-lookup"><span data-stu-id="edc44-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="edc44-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="edc44-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="edc44-114">Questi comandi restituiscono tutte le intestazioni di risposta disponibili.</span><span class="sxs-lookup"><span data-stu-id="edc44-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="edc44-115">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="edc44-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="edc44-116">Questi comandi restituiscono tutte le variabili server disponibili, le intestazioni di richiesta e risposta.</span><span class="sxs-lookup"><span data-stu-id="edc44-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="edc44-117">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="edc44-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="edc44-118">Questi comandi restituiscono tutte le variabili server disponibili, le intestazioni di richiesta e risposta.</span><span class="sxs-lookup"><span data-stu-id="edc44-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="edc44-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="edc44-119">PARAMETERS</span></span>

### <span data-ttu-id="edc44-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc44-120">-DefaultProfile</span></span>
<span data-ttu-id="edc44-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="edc44-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edc44-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="edc44-122">-RequestHeader</span></span>
<span data-ttu-id="edc44-123">Intestazioni delle richieste disponibili per Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="edc44-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="edc44-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="edc44-124">-ResponseHeader</span></span>
<span data-ttu-id="edc44-125">Intestazioni di risposta disponibili in Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="edc44-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="edc44-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="edc44-126">-ServerVariable</span></span>
<span data-ttu-id="edc44-127">Variabili server disponibili in Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="edc44-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="edc44-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc44-128">CommonParameters</span></span>
<span data-ttu-id="edc44-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edc44-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc44-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edc44-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc44-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="edc44-131">INPUTS</span></span>

### <span data-ttu-id="edc44-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="edc44-132">None</span></span>

## <span data-ttu-id="edc44-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="edc44-133">OUTPUTS</span></span>

### <span data-ttu-id="edc44-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="edc44-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="edc44-135">Note</span><span class="sxs-lookup"><span data-stu-id="edc44-135">NOTES</span></span>
<span data-ttu-id="edc44-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** è un alias per il cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .</span><span class="sxs-lookup"><span data-stu-id="edc44-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="edc44-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="edc44-137">RELATED LINKS</span></span>
