---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d075c6792134536be84643d51f37b2379b63d5e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674800"
---
# <span data-ttu-id="e73ac-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e73ac-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="e73ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e73ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e73ac-103">Ottiene il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="e73ac-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="e73ac-104">Se non viene specificato alcun provider, elenca tutti i provider per l'account.</span><span class="sxs-lookup"><span data-stu-id="e73ac-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="e73ac-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e73ac-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e73ac-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e73ac-106">DESCRIPTION</span></span>
<span data-ttu-id="e73ac-107">Il cmdlet **Get-AzDataLakeStoreTrustedIdProvider** ottiene il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="e73ac-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="e73ac-108">Se non viene specificato alcun provider, elenca tutti i provider per l'account.</span><span class="sxs-lookup"><span data-stu-id="e73ac-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="e73ac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e73ac-109">EXAMPLES</span></span>

### <span data-ttu-id="e73ac-110">Esempio 1: ottenere un provider di identità attendibile specifico</span><span class="sxs-lookup"><span data-stu-id="e73ac-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="e73ac-111">Restituisce il provider denominato "metodo di fornitura" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="e73ac-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="e73ac-112">Esempio 2: elenca tutti i provider in un account</span><span class="sxs-lookup"><span data-stu-id="e73ac-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="e73ac-113">Elenca tutti i provider sotto l'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="e73ac-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="e73ac-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e73ac-114">PARAMETERS</span></span>

### <span data-ttu-id="e73ac-115">-Account</span><span class="sxs-lookup"><span data-stu-id="e73ac-115">-Account</span></span>
<span data-ttu-id="e73ac-116">L'account di data Lake Store per recuperare il provider di identità attendibile da</span><span class="sxs-lookup"><span data-stu-id="e73ac-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="e73ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73ac-117">-DefaultProfile</span></span>
<span data-ttu-id="e73ac-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e73ac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e73ac-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e73ac-119">-Name</span></span>
<span data-ttu-id="e73ac-120">Nome del provider di identità attendibile da recuperare</span><span class="sxs-lookup"><span data-stu-id="e73ac-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="e73ac-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73ac-121">-ResourceGroupName</span></span>
<span data-ttu-id="e73ac-122">Nome del gruppo di risorse in cui si vuole recuperare il provider di identità attendibile specificato dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="e73ac-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="e73ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73ac-123">CommonParameters</span></span>
<span data-ttu-id="e73ac-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73ac-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e73ac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73ac-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e73ac-126">INPUTS</span></span>

### <span data-ttu-id="e73ac-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e73ac-127">System.String</span></span>

## <span data-ttu-id="e73ac-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e73ac-128">OUTPUTS</span></span>

### <span data-ttu-id="e73ac-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="e73ac-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="e73ac-130">Note</span><span class="sxs-lookup"><span data-stu-id="e73ac-130">NOTES</span></span>

## <span data-ttu-id="e73ac-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e73ac-131">RELATED LINKS</span></span>
