---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189090"
---
# <span data-ttu-id="813fa-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="813fa-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="813fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="813fa-102">SYNOPSIS</span></span>
<span data-ttu-id="813fa-103">Ottiene i dettagli di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="813fa-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="813fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="813fa-104">SYNTAX</span></span>

### <span data-ttu-id="813fa-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="813fa-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="813fa-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="813fa-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="813fa-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="813fa-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="813fa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="813fa-108">DESCRIPTION</span></span>
<span data-ttu-id="813fa-109">Il cmdlet **Get-AzDataLakeStoreAccount** ottiene i dettagli di un account di archivio dati per i laghi.</span><span class="sxs-lookup"><span data-stu-id="813fa-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="813fa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="813fa-110">EXAMPLES</span></span>

### <span data-ttu-id="813fa-111">Esempio 1: ottenere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="813fa-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="813fa-112">Questo comando consente di ottenere l'account denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="813fa-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="813fa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="813fa-113">PARAMETERS</span></span>

### <span data-ttu-id="813fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813fa-114">-DefaultProfile</span></span>
<span data-ttu-id="813fa-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="813fa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="813fa-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="813fa-116">-Name</span></span>
<span data-ttu-id="813fa-117">Specifica il nome dell'account da ottenere.</span><span class="sxs-lookup"><span data-stu-id="813fa-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="813fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="813fa-119">Specifica il nome del gruppo di risorse che contiene l'account di data Lake Store da ottenere.</span><span class="sxs-lookup"><span data-stu-id="813fa-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="813fa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813fa-120">CommonParameters</span></span>
<span data-ttu-id="813fa-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="813fa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813fa-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="813fa-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813fa-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="813fa-123">INPUTS</span></span>

### <span data-ttu-id="813fa-124">System. String</span><span class="sxs-lookup"><span data-stu-id="813fa-124">System.String</span></span>

## <span data-ttu-id="813fa-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="813fa-125">OUTPUTS</span></span>

### <span data-ttu-id="813fa-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="813fa-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="813fa-127">Note</span><span class="sxs-lookup"><span data-stu-id="813fa-127">NOTES</span></span>

## <span data-ttu-id="813fa-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="813fa-128">RELATED LINKS</span></span>

[<span data-ttu-id="813fa-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="813fa-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="813fa-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="813fa-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="813fa-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="813fa-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="813fa-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="813fa-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


