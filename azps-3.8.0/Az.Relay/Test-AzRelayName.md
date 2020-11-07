---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865099"
---
# <span data-ttu-id="0817f-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="0817f-101">Test-AzRelayName</span></span>

## <span data-ttu-id="0817f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0817f-102">SYNOPSIS</span></span>
<span data-ttu-id="0817f-103">Controlla la disponibilità del nome dello spazio dei nomi assegnato</span><span class="sxs-lookup"><span data-stu-id="0817f-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="0817f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0817f-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0817f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0817f-105">DESCRIPTION</span></span>
<span data-ttu-id="0817f-106">Il cmdlet **test-AzRelayName** verifica la disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0817f-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="0817f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0817f-107">EXAMPLES</span></span>

### <span data-ttu-id="0817f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0817f-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="0817f-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0817f-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="0817f-110">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0817f-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="0817f-111">Restituisce lo stato della disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0817f-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="0817f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0817f-112">PARAMETERS</span></span>

### <span data-ttu-id="0817f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0817f-113">-DefaultProfile</span></span>
<span data-ttu-id="0817f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0817f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0817f-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0817f-115">-Namespace</span></span>
<span data-ttu-id="0817f-116">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="0817f-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="0817f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0817f-117">CommonParameters</span></span>
<span data-ttu-id="0817f-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0817f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0817f-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0817f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0817f-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0817f-120">INPUTS</span></span>

### <span data-ttu-id="0817f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0817f-121">System.String</span></span>

## <span data-ttu-id="0817f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0817f-122">OUTPUTS</span></span>

### <span data-ttu-id="0817f-123">Microsoft. Azure. Commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="0817f-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="0817f-124">Note</span><span class="sxs-lookup"><span data-stu-id="0817f-124">NOTES</span></span>

## <span data-ttu-id="0817f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0817f-125">RELATED LINKS</span></span>
