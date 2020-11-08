---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200003"
---
# <span data-ttu-id="e4609-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="e4609-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="e4609-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4609-102">SYNOPSIS</span></span>
<span data-ttu-id="e4609-103">Elenco delle operazioni di ServiceBus supportate</span><span class="sxs-lookup"><span data-stu-id="e4609-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="e4609-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4609-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4609-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4609-105">DESCRIPTION</span></span>
<span data-ttu-id="e4609-106">Il cmdlet **Get-AzServiceBusOperation** elenca le operazioni supportate da ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="e4609-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="e4609-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4609-107">EXAMPLES</span></span>

### <span data-ttu-id="e4609-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4609-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="e4609-109">Elenca le operazioni supportate da ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e4609-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="e4609-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4609-110">PARAMETERS</span></span>

### <span data-ttu-id="e4609-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4609-111">-DefaultProfile</span></span>
<span data-ttu-id="e4609-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4609-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4609-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4609-113">CommonParameters</span></span>
<span data-ttu-id="e4609-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4609-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4609-115">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4609-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4609-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4609-116">INPUTS</span></span>

### <span data-ttu-id="e4609-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e4609-117">None</span></span>

## <span data-ttu-id="e4609-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4609-118">OUTPUTS</span></span>

### <span data-ttu-id="e4609-119">Microsoft. Azure. Commands. ServiceBus. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="e4609-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="e4609-120">Note</span><span class="sxs-lookup"><span data-stu-id="e4609-120">NOTES</span></span>

## <span data-ttu-id="e4609-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4609-121">RELATED LINKS</span></span>