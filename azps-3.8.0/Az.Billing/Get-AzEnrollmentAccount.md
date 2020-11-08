---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020363"
---
# <span data-ttu-id="b1279-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="b1279-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="b1279-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1279-102">SYNOPSIS</span></span>
<span data-ttu-id="b1279-103">Ottenere gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b1279-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="b1279-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1279-104">SYNTAX</span></span>

### <span data-ttu-id="b1279-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1279-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1279-106">Singola</span><span class="sxs-lookup"><span data-stu-id="b1279-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1279-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1279-107">DESCRIPTION</span></span>
<span data-ttu-id="b1279-108">Il cmdlet **Get-AzEnrollmentAccount** ottiene gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b1279-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="b1279-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1279-109">EXAMPLES</span></span>

### <span data-ttu-id="b1279-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1279-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="b1279-111">Ottenere tutti gli account di registrazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="b1279-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="b1279-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b1279-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="b1279-113">Ottenere l'account di registrazione con l'ID oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="b1279-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="b1279-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1279-114">PARAMETERS</span></span>

### <span data-ttu-id="b1279-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1279-115">-DefaultProfile</span></span>
<span data-ttu-id="b1279-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b1279-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1279-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b1279-117">-ObjectId</span></span>
<span data-ttu-id="b1279-118">ObjectId di un account di registrazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b1279-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="b1279-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1279-119">CommonParameters</span></span>
<span data-ttu-id="b1279-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1279-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1279-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1279-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1279-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1279-122">INPUTS</span></span>

### <span data-ttu-id="b1279-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b1279-123">None</span></span>

## <span data-ttu-id="b1279-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1279-124">OUTPUTS</span></span>

### <span data-ttu-id="b1279-125">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="b1279-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="b1279-126">Note</span><span class="sxs-lookup"><span data-stu-id="b1279-126">NOTES</span></span>

## <span data-ttu-id="b1279-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1279-127">RELATED LINKS</span></span>
