---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208571"
---
# <span data-ttu-id="13fa0-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="13fa0-101">Test-AzRelayName</span></span>

## <span data-ttu-id="13fa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="13fa0-103">Controlla la disponibilità del nome namespace specificato</span><span class="sxs-lookup"><span data-stu-id="13fa0-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="13fa0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13fa0-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13fa0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="13fa0-106">Il **cmdlet Test-AzRelayName** controlla la disponibilità del nome NameSpace</span><span class="sxs-lookup"><span data-stu-id="13fa0-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="13fa0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13fa0-107">EXAMPLES</span></span>

### <span data-ttu-id="13fa0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13fa0-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="13fa0-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="13fa0-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="13fa0-110">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="13fa0-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="13fa0-111">Restituisce lo stato in base alla disponibilità del nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13fa0-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="13fa0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13fa0-112">PARAMETERS</span></span>

### <span data-ttu-id="13fa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13fa0-113">-DefaultProfile</span></span>
<span data-ttu-id="13fa0-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13fa0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13fa0-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13fa0-115">-Namespace</span></span>
<span data-ttu-id="13fa0-116">Relay Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="13fa0-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="13fa0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fa0-117">CommonParameters</span></span>
<span data-ttu-id="13fa0-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13fa0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fa0-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13fa0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fa0-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="13fa0-120">INPUTS</span></span>

### <span data-ttu-id="13fa0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="13fa0-121">System.String</span></span>

## <span data-ttu-id="13fa0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13fa0-122">OUTPUTS</span></span>

### <span data-ttu-id="13fa0-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="13fa0-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="13fa0-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="13fa0-124">NOTES</span></span>

## <span data-ttu-id="13fa0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13fa0-125">RELATED LINKS</span></span>
