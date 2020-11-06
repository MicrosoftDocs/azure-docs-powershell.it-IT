---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509080"
---
# <span data-ttu-id="c553d-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="c553d-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="c553d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c553d-102">SYNOPSIS</span></span>
<span data-ttu-id="c553d-103">Ottiene la posizione in cui Azure Security Center salverà automaticamente i dati per l'abbonamento specifico</span><span class="sxs-lookup"><span data-stu-id="c553d-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c553d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c553d-104">SYNTAX</span></span>

### <span data-ttu-id="c553d-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c553d-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c553d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c553d-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c553d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c553d-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c553d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c553d-108">DESCRIPTION</span></span>
<span data-ttu-id="c553d-109">Azure Security Center deciderà automaticamente in un percorso per salvare alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="c553d-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="c553d-110">Usa questo cmdlet per scoprire la posizione.</span><span class="sxs-lookup"><span data-stu-id="c553d-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="c553d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c553d-111">EXAMPLES</span></span>

### <span data-ttu-id="c553d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c553d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="c553d-113">Ottiene la posizione in cui Azure Security Center Salva i dati di sicurezza calcolati.</span><span class="sxs-lookup"><span data-stu-id="c553d-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="c553d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c553d-114">PARAMETERS</span></span>

### <span data-ttu-id="c553d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c553d-115">-DefaultProfile</span></span>
<span data-ttu-id="c553d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c553d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c553d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c553d-117">-Name</span></span>
<span data-ttu-id="c553d-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="c553d-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c553d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c553d-119">-ResourceId</span></span>
<span data-ttu-id="c553d-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c553d-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c553d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c553d-121">CommonParameters</span></span>
<span data-ttu-id="c553d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c553d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c553d-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c553d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c553d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c553d-124">INPUTS</span></span>

### <span data-ttu-id="c553d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c553d-125">System.String</span></span>

## <span data-ttu-id="c553d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c553d-126">OUTPUTS</span></span>

### <span data-ttu-id="c553d-127">Microsoft. Azure. Commands. Security. Models. locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="c553d-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="c553d-128">Note</span><span class="sxs-lookup"><span data-stu-id="c553d-128">NOTES</span></span>

## <span data-ttu-id="c553d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c553d-129">RELATED LINKS</span></span>
