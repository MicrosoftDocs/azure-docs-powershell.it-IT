---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486348"
---
# <span data-ttu-id="58a32-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="58a32-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="58a32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58a32-102">SYNOPSIS</span></span>
<span data-ttu-id="58a32-103">Ottiene i tipi di valutazione della sicurezza e metadta in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="58a32-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="58a32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58a32-104">SYNTAX</span></span>

### <span data-ttu-id="58a32-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58a32-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58a32-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="58a32-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58a32-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a32-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58a32-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58a32-108">DESCRIPTION</span></span>
<span data-ttu-id="58a32-109">Ottiene i tipi di valutazione della sicurezza e metadta in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="58a32-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="58a32-110">I metadati per la valutazione della sicurezza includono Built-In valutazioni e tipi di valutazione personalizzati che l'utente può definire.</span><span class="sxs-lookup"><span data-stu-id="58a32-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="58a32-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58a32-111">EXAMPLES</span></span>

### <span data-ttu-id="58a32-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58a32-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="58a32-113">Ottiene tutte le valutazioni predefinite e le valutazioni personalizzate configurate nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="58a32-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="58a32-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58a32-114">PARAMETERS</span></span>

### <span data-ttu-id="58a32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a32-115">-DefaultProfile</span></span>
<span data-ttu-id="58a32-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58a32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58a32-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="58a32-117">-Name</span></span>
<span data-ttu-id="58a32-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="58a32-118">Resource name.</span></span>

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

### <span data-ttu-id="58a32-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a32-119">-ResourceId</span></span>
<span data-ttu-id="58a32-120">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="58a32-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="58a32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a32-121">CommonParameters</span></span>
<span data-ttu-id="58a32-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a32-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58a32-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a32-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58a32-124">INPUTS</span></span>

### <span data-ttu-id="58a32-125">System. String</span><span class="sxs-lookup"><span data-stu-id="58a32-125">System.String</span></span>

## <span data-ttu-id="58a32-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58a32-126">OUTPUTS</span></span>

### <span data-ttu-id="58a32-127">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="58a32-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="58a32-128">Note</span><span class="sxs-lookup"><span data-stu-id="58a32-128">NOTES</span></span>

## <span data-ttu-id="58a32-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58a32-129">RELATED LINKS</span></span>
