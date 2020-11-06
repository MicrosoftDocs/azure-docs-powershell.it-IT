---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 4b3afc0b41f6eaf68e7ec0c4f8ed976b36267c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510360"
---
# <span data-ttu-id="28564-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="28564-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="28564-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28564-102">SYNOPSIS</span></span>
<span data-ttu-id="28564-103">Controlla la disponibilità del nome dello spazio dei nomi assegnato</span><span class="sxs-lookup"><span data-stu-id="28564-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28564-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28564-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28564-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28564-105">DESCRIPTION</span></span>
<span data-ttu-id="28564-106">Il cmdlet **test-AzureRmRelayName** verifica la disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28564-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="28564-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28564-107">EXAMPLES</span></span>

### <span data-ttu-id="28564-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28564-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="28564-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="28564-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="28564-110">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="28564-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="28564-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28564-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="28564-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28564-112">PARAMETERS</span></span>

### <span data-ttu-id="28564-113">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28564-113">-Namespace</span></span>
<span data-ttu-id="28564-114">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="28564-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28564-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28564-115">-DefaultProfile</span></span>
<span data-ttu-id="28564-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28564-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28564-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28564-117">CommonParameters</span></span>
<span data-ttu-id="28564-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28564-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28564-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28564-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28564-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28564-120">INPUTS</span></span>

### <span data-ttu-id="28564-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="28564-121">-Namespace</span></span>
 <span data-ttu-id="28564-122">System. String</span><span class="sxs-lookup"><span data-stu-id="28564-122">System.String</span></span>

## <span data-ttu-id="28564-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28564-123">OUTPUTS</span></span>

### <span data-ttu-id="28564-124">[Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="28564-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="28564-125">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28564-125">Example 1</span></span>
<span data-ttu-id="28564-126">Messaggio motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="28564-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="28564-127">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="28564-127">Example 2</span></span>
<span data-ttu-id="28564-128">Messaggio motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="28564-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="28564-129">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="28564-129">Example 3</span></span>
<span data-ttu-id="28564-130">Messaggio motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="28564-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="28564-131">Note</span><span class="sxs-lookup"><span data-stu-id="28564-131">NOTES</span></span>

## <span data-ttu-id="28564-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28564-132">RELATED LINKS</span></span>

