---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: fbbac617687712208730393b978a3df5b404aeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516012"
---
# <span data-ttu-id="b63ba-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="b63ba-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="b63ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b63ba-102">SYNOPSIS</span></span>
<span data-ttu-id="b63ba-103">Elenco delle operazioni di ServiceBus supportate</span><span class="sxs-lookup"><span data-stu-id="b63ba-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b63ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b63ba-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b63ba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b63ba-105">DESCRIPTION</span></span>
<span data-ttu-id="b63ba-106">Il cmdlet **Get-AzureRmServiceBusOperation** elenca le operazioni supportate da ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="b63ba-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="b63ba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b63ba-107">EXAMPLES</span></span>

### <span data-ttu-id="b63ba-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b63ba-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="b63ba-109">Elenca le operazioni supportate da ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b63ba-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="b63ba-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b63ba-110">PARAMETERS</span></span>

### <span data-ttu-id="b63ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b63ba-111">-DefaultProfile</span></span>
<span data-ttu-id="b63ba-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b63ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b63ba-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b63ba-113">CommonParameters</span></span>
<span data-ttu-id="b63ba-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b63ba-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b63ba-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b63ba-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b63ba-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b63ba-116">INPUTS</span></span>

### <span data-ttu-id="b63ba-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b63ba-117">None</span></span>

### <span data-ttu-id="b63ba-118">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. OperationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b63ba-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b63ba-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b63ba-119">OUTPUTS</span></span>

### <span data-ttu-id="b63ba-120">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. ServiceBus. Models. OperationAttributes]</span><span class="sxs-lookup"><span data-stu-id="b63ba-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="b63ba-121">Note</span><span class="sxs-lookup"><span data-stu-id="b63ba-121">NOTES</span></span>

## <span data-ttu-id="b63ba-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b63ba-122">RELATED LINKS</span></span>

