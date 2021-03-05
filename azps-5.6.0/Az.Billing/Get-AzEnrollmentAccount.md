---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d05499ded326787b9930574872dd0681f773d1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992933"
---
# <span data-ttu-id="1b164-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="1b164-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="1b164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b164-102">SYNOPSIS</span></span>
<span data-ttu-id="1b164-103">Ottenere gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="1b164-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="1b164-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b164-104">SYNTAX</span></span>

### <span data-ttu-id="1b164-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b164-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b164-106">Single</span><span class="sxs-lookup"><span data-stu-id="1b164-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b164-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1b164-107">DESCRIPTION</span></span>
<span data-ttu-id="1b164-108">Il cmdlet **Get-AzEnrollmentAccount** ottiene gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="1b164-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="1b164-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b164-109">EXAMPLES</span></span>

### <span data-ttu-id="1b164-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b164-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="1b164-111">Ottenere tutti gli account di registrazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="1b164-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="1b164-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1b164-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="1b164-113">Ottenere l'account di registrazione con l'ID oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="1b164-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="1b164-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b164-114">PARAMETERS</span></span>

### <span data-ttu-id="1b164-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b164-115">-DefaultProfile</span></span>
<span data-ttu-id="1b164-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1b164-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b164-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1b164-117">-ObjectId</span></span>
<span data-ttu-id="1b164-118">ObjectId di un account di registrazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="1b164-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b164-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b164-119">CommonParameters</span></span>
<span data-ttu-id="1b164-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b164-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b164-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b164-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b164-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="1b164-122">INPUTS</span></span>

### <span data-ttu-id="1b164-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b164-123">None</span></span>

## <span data-ttu-id="1b164-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b164-124">OUTPUTS</span></span>

### <span data-ttu-id="1b164-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="1b164-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="1b164-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="1b164-126">NOTES</span></span>

## <span data-ttu-id="1b164-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b164-127">RELATED LINKS</span></span>
