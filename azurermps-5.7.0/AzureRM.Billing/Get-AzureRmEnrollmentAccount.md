---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510087"
---
# <span data-ttu-id="584bc-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="584bc-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="584bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="584bc-102">SYNOPSIS</span></span>
<span data-ttu-id="584bc-103">Ottenere gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="584bc-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="584bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="584bc-104">SYNTAX</span></span>

### <span data-ttu-id="584bc-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="584bc-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="584bc-106">Singola</span><span class="sxs-lookup"><span data-stu-id="584bc-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="584bc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="584bc-107">DESCRIPTION</span></span>
<span data-ttu-id="584bc-108">Il cmdlet **Get-AzureRmEnrollmentAccount** ottiene gli account di registrazione.</span><span class="sxs-lookup"><span data-stu-id="584bc-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="584bc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="584bc-109">EXAMPLES</span></span>

### <span data-ttu-id="584bc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="584bc-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="584bc-111">Ottenere tutti gli account di registrazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="584bc-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="584bc-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="584bc-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="584bc-113">Ottenere l'account di registrazione con l'ID oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="584bc-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="584bc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="584bc-114">PARAMETERS</span></span>

### <span data-ttu-id="584bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="584bc-115">-DefaultProfile</span></span>
<span data-ttu-id="584bc-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="584bc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="584bc-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="584bc-117">-ObjectId</span></span>
<span data-ttu-id="584bc-118">ObjectId di un account di registrazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="584bc-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="584bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="584bc-119">CommonParameters</span></span>
<span data-ttu-id="584bc-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="584bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="584bc-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="584bc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="584bc-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="584bc-122">INPUTS</span></span>

### <span data-ttu-id="584bc-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="584bc-123">None</span></span>

## <span data-ttu-id="584bc-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="584bc-124">OUTPUTS</span></span>

### <span data-ttu-id="584bc-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Billing. Models. PSEnrollmentAccount, Microsoft. Azure. Commands. Billing, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="584bc-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="584bc-126">Microsoft. Azure. Commands. Billing. Models. PSEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="584bc-126">Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount</span></span>

## <span data-ttu-id="584bc-127">Note</span><span class="sxs-lookup"><span data-stu-id="584bc-127">NOTES</span></span>

## <span data-ttu-id="584bc-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="584bc-128">RELATED LINKS</span></span>

