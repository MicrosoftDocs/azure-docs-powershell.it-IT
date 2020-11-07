---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687687"
---
# <span data-ttu-id="147a4-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="147a4-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="147a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="147a4-102">SYNOPSIS</span></span>
<span data-ttu-id="147a4-103">Controlla la disponibilità del nome dello spazio dei nomi assegnato</span><span class="sxs-lookup"><span data-stu-id="147a4-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="147a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="147a4-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="147a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="147a4-105">DESCRIPTION</span></span>
<span data-ttu-id="147a4-106">Il cmdlet **test-AzureRmServiceBusName** verifica la disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="147a4-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="147a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="147a4-107">EXAMPLES</span></span>

### <span data-ttu-id="147a4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="147a4-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="147a4-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="147a4-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="147a4-110">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="147a4-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="147a4-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="147a4-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="147a4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="147a4-112">PARAMETERS</span></span>

### <span data-ttu-id="147a4-113">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="147a4-113">-Namespace</span></span>
<span data-ttu-id="147a4-114">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="147a4-114">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="147a4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147a4-115">CommonParameters</span></span>
<span data-ttu-id="147a4-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="147a4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147a4-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="147a4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147a4-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="147a4-118">INPUTS</span></span>

### <span data-ttu-id="147a4-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="147a4-119">-Namespace</span></span>
 <span data-ttu-id="147a4-120">System. String</span><span class="sxs-lookup"><span data-stu-id="147a4-120">System.String</span></span>

## <span data-ttu-id="147a4-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="147a4-121">OUTPUTS</span></span>

### <span data-ttu-id="147a4-122">[Microsoft. Azure. Commands. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="147a4-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="147a4-123">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="147a4-123">Example 1</span></span>
<span data-ttu-id="147a4-124">Messaggio motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="147a4-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="147a4-125">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="147a4-125">Example 2</span></span>
<span data-ttu-id="147a4-126">Messaggio motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="147a4-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="147a4-127">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="147a4-127">Example 3</span></span>
<span data-ttu-id="147a4-128">Messaggio motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="147a4-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="147a4-129">Note</span><span class="sxs-lookup"><span data-stu-id="147a4-129">NOTES</span></span>

## <span data-ttu-id="147a4-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="147a4-130">RELATED LINKS</span></span>
