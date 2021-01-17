---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: fb600edb4fd8d18ee82cb7f83d651e6588acaa42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473578"
---
# <span data-ttu-id="67187-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="67187-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="67187-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67187-102">SYNOPSIS</span></span>
<span data-ttu-id="67187-103">Ottiene il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="67187-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="67187-104">Se non viene specificato alcun provider, elenca tutti i provider per l'account.</span><span class="sxs-lookup"><span data-stu-id="67187-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="67187-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67187-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67187-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67187-106">DESCRIPTION</span></span>
<span data-ttu-id="67187-107">Il cmdlet **Get-AzDataLakeStoreTrustedIdProvider** ottiene il provider di identità attendibile specificato nell'archivio dati specificato del lago.</span><span class="sxs-lookup"><span data-stu-id="67187-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="67187-108">Se non viene specificato alcun provider, elenca tutti i provider per l'account.</span><span class="sxs-lookup"><span data-stu-id="67187-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="67187-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67187-109">EXAMPLES</span></span>

### <span data-ttu-id="67187-110">Esempio 1: ottenere un provider di identità attendibile specifico</span><span class="sxs-lookup"><span data-stu-id="67187-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="67187-111">Restituisce il provider denominato "metodo di fornitura" dall'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="67187-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="67187-112">Esempio 2: elenca tutti i provider in un account</span><span class="sxs-lookup"><span data-stu-id="67187-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="67187-113">Elenca tutti i provider sotto l'account "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="67187-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="67187-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67187-114">PARAMETERS</span></span>

### <span data-ttu-id="67187-115">-Account</span><span class="sxs-lookup"><span data-stu-id="67187-115">-Account</span></span>
<span data-ttu-id="67187-116">L'account di data Lake Store per recuperare il provider di identità attendibile da</span><span class="sxs-lookup"><span data-stu-id="67187-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="67187-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67187-117">-DefaultProfile</span></span>
<span data-ttu-id="67187-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="67187-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67187-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="67187-119">-Name</span></span>
<span data-ttu-id="67187-120">Nome del provider di identità attendibile da recuperare</span><span class="sxs-lookup"><span data-stu-id="67187-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="67187-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67187-121">-ResourceGroupName</span></span>
<span data-ttu-id="67187-122">Nome del gruppo di risorse in cui si vuole recuperare il provider di identità attendibile specificato dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="67187-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="67187-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67187-123">CommonParameters</span></span>
<span data-ttu-id="67187-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67187-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67187-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67187-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67187-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67187-126">INPUTS</span></span>

### <span data-ttu-id="67187-127">System. String</span><span class="sxs-lookup"><span data-stu-id="67187-127">System.String</span></span>

## <span data-ttu-id="67187-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67187-128">OUTPUTS</span></span>

### <span data-ttu-id="67187-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="67187-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="67187-130">Note</span><span class="sxs-lookup"><span data-stu-id="67187-130">NOTES</span></span>

## <span data-ttu-id="67187-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67187-131">RELATED LINKS</span></span>
