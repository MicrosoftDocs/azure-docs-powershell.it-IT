---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519704"
---
# <span data-ttu-id="49e5c-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="49e5c-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="49e5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="49e5c-103">Controlla la disponibilità del nome dello spazio dei nomi assegnato</span><span class="sxs-lookup"><span data-stu-id="49e5c-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49e5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49e5c-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49e5c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49e5c-105">DESCRIPTION</span></span>
<span data-ttu-id="49e5c-106">Il cmdlet **test-AzureRmRelayName** verifica la disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49e5c-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="49e5c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49e5c-107">EXAMPLES</span></span>

### <span data-ttu-id="49e5c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49e5c-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="49e5c-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="49e5c-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="49e5c-110">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="49e5c-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="49e5c-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49e5c-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="49e5c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49e5c-112">PARAMETERS</span></span>

### <span data-ttu-id="49e5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49e5c-113">-DefaultProfile</span></span>
<span data-ttu-id="49e5c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49e5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49e5c-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49e5c-115">-Namespace</span></span>
<span data-ttu-id="49e5c-116">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="49e5c-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="49e5c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49e5c-117">CommonParameters</span></span>
<span data-ttu-id="49e5c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49e5c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="49e5c-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49e5c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49e5c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49e5c-120">INPUTS</span></span>

### <span data-ttu-id="49e5c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="49e5c-121">System.String</span></span>


## <span data-ttu-id="49e5c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49e5c-122">OUTPUTS</span></span>

### <span data-ttu-id="49e5c-123">Microsoft. Azure. Commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="49e5c-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="49e5c-124">Note</span><span class="sxs-lookup"><span data-stu-id="49e5c-124">NOTES</span></span>

## <span data-ttu-id="49e5c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49e5c-125">RELATED LINKS</span></span>
