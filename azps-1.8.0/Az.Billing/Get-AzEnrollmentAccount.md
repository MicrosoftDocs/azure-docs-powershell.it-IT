---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d76797f82a14c8efa2f9a3d6a77436fa2f8a1b68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684905"
---
# <span data-ttu-id="f8074-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="f8074-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="f8074-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8074-102">SYNOPSIS</span></span>
<span data-ttu-id="f8074-103">Ottenere gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f8074-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="f8074-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8074-104">SYNTAX</span></span>

### <span data-ttu-id="f8074-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8074-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8074-106">Singola</span><span class="sxs-lookup"><span data-stu-id="f8074-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8074-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8074-107">DESCRIPTION</span></span>
<span data-ttu-id="f8074-108">Il cmdlet **Get-AzEnrollmentAccount** ottiene gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f8074-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="f8074-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8074-109">EXAMPLES</span></span>

### <span data-ttu-id="f8074-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8074-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="f8074-111">Ottenere tutti gli account di registrazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="f8074-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="f8074-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f8074-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="f8074-113">Ottenere l'account di registrazione con l'ID oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="f8074-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="f8074-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8074-114">PARAMETERS</span></span>

### <span data-ttu-id="f8074-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8074-115">-DefaultProfile</span></span>
<span data-ttu-id="f8074-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f8074-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8074-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f8074-117">-ObjectId</span></span>
<span data-ttu-id="f8074-118">ObjectId di un account di registrazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f8074-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="f8074-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8074-119">CommonParameters</span></span>
<span data-ttu-id="f8074-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8074-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8074-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8074-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8074-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8074-122">INPUTS</span></span>

### <span data-ttu-id="f8074-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f8074-123">None</span></span>

## <span data-ttu-id="f8074-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8074-124">OUTPUTS</span></span>

### <span data-ttu-id="f8074-125">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="f8074-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="f8074-126">Note</span><span class="sxs-lookup"><span data-stu-id="f8074-126">NOTES</span></span>

## <span data-ttu-id="f8074-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8074-127">RELATED LINKS</span></span>
