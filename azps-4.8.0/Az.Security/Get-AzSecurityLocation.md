---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: 77f9283b16aa605da066780165c2fe7b42b1830b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188861"
---
# <span data-ttu-id="56ed3-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="56ed3-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="56ed3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="56ed3-103">Ottiene la posizione in cui Azure Security Center salverà automaticamente i dati per l'abbonamento specifico</span><span class="sxs-lookup"><span data-stu-id="56ed3-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="56ed3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56ed3-104">SYNTAX</span></span>

### <span data-ttu-id="56ed3-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56ed3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56ed3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="56ed3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56ed3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="56ed3-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56ed3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56ed3-108">DESCRIPTION</span></span>
<span data-ttu-id="56ed3-109">Azure Security Center deciderà automaticamente in un percorso per salvare alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="56ed3-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="56ed3-110">Usa questo cmdlet per scoprire la posizione.</span><span class="sxs-lookup"><span data-stu-id="56ed3-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="56ed3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56ed3-111">EXAMPLES</span></span>

### <span data-ttu-id="56ed3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56ed3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="56ed3-113">Ottiene la posizione in cui Azure Security Center Salva i dati di sicurezza calcolati.</span><span class="sxs-lookup"><span data-stu-id="56ed3-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="56ed3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56ed3-114">PARAMETERS</span></span>

### <span data-ttu-id="56ed3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ed3-115">-DefaultProfile</span></span>
<span data-ttu-id="56ed3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56ed3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ed3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="56ed3-117">-Name</span></span>
<span data-ttu-id="56ed3-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="56ed3-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ed3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56ed3-119">-ResourceId</span></span>
<span data-ttu-id="56ed3-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="56ed3-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56ed3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ed3-121">CommonParameters</span></span>
<span data-ttu-id="56ed3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ed3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ed3-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56ed3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ed3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56ed3-124">INPUTS</span></span>

### <span data-ttu-id="56ed3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="56ed3-125">System.String</span></span>

## <span data-ttu-id="56ed3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56ed3-126">OUTPUTS</span></span>

### <span data-ttu-id="56ed3-127">Microsoft. Azure. Commands. Security. Models. locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="56ed3-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="56ed3-128">Note</span><span class="sxs-lookup"><span data-stu-id="56ed3-128">NOTES</span></span>

## <span data-ttu-id="56ed3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56ed3-129">RELATED LINKS</span></span>