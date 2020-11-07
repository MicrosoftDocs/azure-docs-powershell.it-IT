---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: bc272648920e29ed2e735ca08b9fa78563a9f9d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686524"
---
# <span data-ttu-id="8807c-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="8807c-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="8807c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8807c-102">SYNOPSIS</span></span>
<span data-ttu-id="8807c-103">Ottiene i dettagli relativi ai tipi di argomenti supportati dalla griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="8807c-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8807c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8807c-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8807c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8807c-105">DESCRIPTION</span></span>
<span data-ttu-id="8807c-106">Ottiene i dettagli dei tipi di argomenti supportati dalla griglia di eventi Azure.</span><span class="sxs-lookup"><span data-stu-id="8807c-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="8807c-107">Se viene specificato un nome tipo di argomento, vengono restituiti i dettagli relativi al tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="8807c-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="8807c-108">Se non si specifica un nome di tipo di argomento, vengono restituiti i dettagli su tutti i tipi di argomenti.</span><span class="sxs-lookup"><span data-stu-id="8807c-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="8807c-109">Se IncludeEventTypes è specificato, nella risposta vengono incluse informazioni sui tipi di evento supportati da ogni tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="8807c-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="8807c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8807c-110">EXAMPLES</span></span>

### <span data-ttu-id="8807c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8807c-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="8807c-112">Ottiene un elenco dei tipi di argomenti.</span><span class="sxs-lookup"><span data-stu-id="8807c-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="8807c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8807c-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="8807c-114">Ottiene le informazioni sul tipo di argomento StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="8807c-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="8807c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8807c-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="8807c-116">Ottiene le informazioni sul tipo di argomento StorageAccounts, inclusi i tipi di evento supportati da StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="8807c-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="8807c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8807c-117">PARAMETERS</span></span>

### <span data-ttu-id="8807c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8807c-118">-DefaultProfile</span></span>
<span data-ttu-id="8807c-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8807c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8807c-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="8807c-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="8807c-121">Se specificato, la risposta includerà i tipi di evento supportati da un tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="8807c-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8807c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8807c-122">-Name</span></span>
<span data-ttu-id="8807c-123">Nome tipo argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8807c-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8807c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8807c-124">CommonParameters</span></span>
<span data-ttu-id="8807c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8807c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8807c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8807c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8807c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8807c-127">INPUTS</span></span>

### <span data-ttu-id="8807c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8807c-128">System.String</span></span>
<span data-ttu-id="8807c-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8807c-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8807c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8807c-130">OUTPUTS</span></span>

### <span data-ttu-id="8807c-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8807c-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="8807c-132">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="8807c-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="8807c-133">Note</span><span class="sxs-lookup"><span data-stu-id="8807c-133">NOTES</span></span>

## <span data-ttu-id="8807c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8807c-134">RELATED LINKS</span></span>
