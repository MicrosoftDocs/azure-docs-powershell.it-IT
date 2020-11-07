---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 950ac2da0d69a11a29d39059f267e9273b783499
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678830"
---
# <span data-ttu-id="5e14c-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="5e14c-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="5e14c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e14c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e14c-103">Ottiene i dettagli relativi ai tipi di argomenti supportati dalla griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e14c-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="5e14c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e14c-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e14c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e14c-105">DESCRIPTION</span></span>
<span data-ttu-id="5e14c-106">Ottiene i dettagli dei tipi di argomenti supportati dalla griglia di eventi Azure.</span><span class="sxs-lookup"><span data-stu-id="5e14c-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="5e14c-107">Se viene specificato un nome tipo di argomento, vengono restituiti i dettagli relativi al tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="5e14c-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="5e14c-108">Se non si specifica un nome di tipo di argomento, vengono restituiti i dettagli su tutti i tipi di argomenti.</span><span class="sxs-lookup"><span data-stu-id="5e14c-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="5e14c-109">Se IncludeEventTypes è specificato, nella risposta vengono incluse informazioni sui tipi di evento supportati da ogni tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="5e14c-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="5e14c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e14c-110">EXAMPLES</span></span>

### <span data-ttu-id="5e14c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e14c-111">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="5e14c-112">Ottiene un elenco dei tipi di argomenti.</span><span class="sxs-lookup"><span data-stu-id="5e14c-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="5e14c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5e14c-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="5e14c-114">Ottiene le informazioni sul tipo di argomento StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="5e14c-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="5e14c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5e14c-115">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="5e14c-116">Ottiene le informazioni sul tipo di argomento StorageAccounts, inclusi i tipi di evento supportati da StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="5e14c-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="5e14c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e14c-117">PARAMETERS</span></span>

### <span data-ttu-id="5e14c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e14c-118">-DefaultProfile</span></span>
<span data-ttu-id="5e14c-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5e14c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e14c-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="5e14c-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="5e14c-121">Se specificato, la risposta includerà i tipi di evento supportati da un tipo di argomento.</span><span class="sxs-lookup"><span data-stu-id="5e14c-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="5e14c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e14c-122">-Name</span></span>
<span data-ttu-id="5e14c-123">Nome tipo argomento EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5e14c-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e14c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e14c-124">CommonParameters</span></span>
<span data-ttu-id="5e14c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e14c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e14c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e14c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e14c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e14c-127">INPUTS</span></span>

### <span data-ttu-id="5e14c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5e14c-128">System.String</span></span>

## <span data-ttu-id="5e14c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e14c-129">OUTPUTS</span></span>

### <span data-ttu-id="5e14c-130">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="5e14c-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="5e14c-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="5e14c-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="5e14c-132">Note</span><span class="sxs-lookup"><span data-stu-id="5e14c-132">NOTES</span></span>

## <span data-ttu-id="5e14c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e14c-133">RELATED LINKS</span></span>
