---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486323"
---
# <span data-ttu-id="c933e-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="c933e-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="c933e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c933e-102">SYNOPSIS</span></span>
<span data-ttu-id="c933e-103">Ottiene le definizioni di controllo del Punteggio sicuro per la sicurezza in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="c933e-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="c933e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c933e-104">SYNTAX</span></span>

### <span data-ttu-id="c933e-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c933e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c933e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c933e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c933e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c933e-107">EXAMPLES</span></span>

### <span data-ttu-id="c933e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c933e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="c933e-109">Ottiene tutte le definizioni di controllo del Punteggio sicuro di sicurezza in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="c933e-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="c933e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c933e-110">PARAMETERS</span></span>

### <span data-ttu-id="c933e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c933e-111">-DefaultProfile</span></span>
<span data-ttu-id="c933e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c933e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c933e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c933e-113">CommonParameters</span></span>
<span data-ttu-id="c933e-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c933e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c933e-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c933e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c933e-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c933e-116">INPUTS</span></span>

### <span data-ttu-id="c933e-117">System. String</span><span class="sxs-lookup"><span data-stu-id="c933e-117">System.String</span></span>

## <span data-ttu-id="c933e-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c933e-118">OUTPUTS</span></span>

### <span data-ttu-id="c933e-119">Microsoft. Azure. Commands. Security. Models. assessments. PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="c933e-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="c933e-120">Note</span><span class="sxs-lookup"><span data-stu-id="c933e-120">NOTES</span></span>

## <span data-ttu-id="c933e-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c933e-121">RELATED LINKS</span></span>
