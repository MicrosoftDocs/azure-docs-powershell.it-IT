---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: ac03d161e8ea786b939f8068dc2efd9109af3ab5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971149"
---
# <span data-ttu-id="53bce-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="53bce-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="53bce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53bce-102">SYNOPSIS</span></span>
<span data-ttu-id="53bce-103">Ottiene il provider di identità attendibile specificato nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="53bce-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="53bce-104">Se non viene specificato alcun provider, vengono elencati tutti i provider per l'account.</span><span class="sxs-lookup"><span data-stu-id="53bce-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="53bce-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53bce-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53bce-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="53bce-106">DESCRIPTION</span></span>
<span data-ttu-id="53bce-107">Il cmdlet **Get-AzDataLakeStoreTrustedIdProvider** ottiene il provider di identità attendibile specificato nel Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="53bce-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="53bce-108">Se non viene specificato alcun provider, vengono elencati tutti i provider per l'account.</span><span class="sxs-lookup"><span data-stu-id="53bce-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="53bce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53bce-109">EXAMPLES</span></span>

### <span data-ttu-id="53bce-110">Esempio 1: Ottenere un provider di identità attendibile specifico</span><span class="sxs-lookup"><span data-stu-id="53bce-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="53bce-111">Restituisce il provider denominato "MyProvider" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="53bce-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="53bce-112">Esempio 2: Elencare tutti i provider in un account</span><span class="sxs-lookup"><span data-stu-id="53bce-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="53bce-113">Elenca tutti i provider nell'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="53bce-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="53bce-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53bce-114">PARAMETERS</span></span>

### <span data-ttu-id="53bce-115">-Account</span><span class="sxs-lookup"><span data-stu-id="53bce-115">-Account</span></span>
<span data-ttu-id="53bce-116">Account Data Lake Store da cui recuperare il provider di identità attendibile</span><span class="sxs-lookup"><span data-stu-id="53bce-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bce-117">-DefaultProfile</span></span>
<span data-ttu-id="53bce-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="53bce-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53bce-119">-Name</span><span class="sxs-lookup"><span data-stu-id="53bce-119">-Name</span></span>
<span data-ttu-id="53bce-120">Nome del provider di identità attendibile da recuperare</span><span class="sxs-lookup"><span data-stu-id="53bce-120">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bce-121">-ResourceGroupName</span></span>
<span data-ttu-id="53bce-122">Nome del gruppo di risorse in cui recuperare il provider di identità attendibile specificato dall'account specificato.</span><span class="sxs-lookup"><span data-stu-id="53bce-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bce-123">CommonParameters</span></span>
<span data-ttu-id="53bce-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bce-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bce-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bce-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="53bce-126">INPUTS</span></span>

### <span data-ttu-id="53bce-127">System.String</span><span class="sxs-lookup"><span data-stu-id="53bce-127">System.String</span></span>

## <span data-ttu-id="53bce-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53bce-128">OUTPUTS</span></span>

### <span data-ttu-id="53bce-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="53bce-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="53bce-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="53bce-130">NOTES</span></span>

## <span data-ttu-id="53bce-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53bce-131">RELATED LINKS</span></span>
