---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182006"
---
# <span data-ttu-id="28cc6-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="28cc6-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="28cc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="28cc6-103">Ottenere gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="28cc6-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="28cc6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28cc6-104">SYNTAX</span></span>

### <span data-ttu-id="28cc6-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28cc6-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28cc6-106">Single</span><span class="sxs-lookup"><span data-stu-id="28cc6-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28cc6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="28cc6-107">DESCRIPTION</span></span>
<span data-ttu-id="28cc6-108">Il cmdlet **Get-AzEnrollmentAccount** ottiene gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="28cc6-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="28cc6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28cc6-109">EXAMPLES</span></span>

### <span data-ttu-id="28cc6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28cc6-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="28cc6-111">Ottenere tutti gli account di registrazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="28cc6-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="28cc6-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="28cc6-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="28cc6-113">Ottenere l'account di registrazione con l'ID oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="28cc6-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="28cc6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28cc6-114">PARAMETERS</span></span>

### <span data-ttu-id="28cc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cc6-115">-DefaultProfile</span></span>
<span data-ttu-id="28cc6-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="28cc6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28cc6-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="28cc6-117">-ObjectId</span></span>
<span data-ttu-id="28cc6-118">ObjectId di un account di registrazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="28cc6-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="28cc6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cc6-119">CommonParameters</span></span>
<span data-ttu-id="28cc6-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28cc6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cc6-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28cc6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cc6-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="28cc6-122">INPUTS</span></span>

### <span data-ttu-id="28cc6-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28cc6-123">None</span></span>

## <span data-ttu-id="28cc6-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28cc6-124">OUTPUTS</span></span>

### <span data-ttu-id="28cc6-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="28cc6-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="28cc6-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="28cc6-126">NOTES</span></span>

## <span data-ttu-id="28cc6-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28cc6-127">RELATED LINKS</span></span>
