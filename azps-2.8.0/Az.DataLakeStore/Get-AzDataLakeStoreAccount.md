---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: b06b64b81679d1f0f9429be0362f936046e54ee5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674819"
---
# <span data-ttu-id="55759-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="55759-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="55759-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55759-102">SYNOPSIS</span></span>
<span data-ttu-id="55759-103">Ottiene i dettagli di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="55759-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="55759-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55759-104">SYNTAX</span></span>

### <span data-ttu-id="55759-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55759-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55759-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="55759-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55759-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="55759-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55759-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55759-108">DESCRIPTION</span></span>
<span data-ttu-id="55759-109">Il cmdlet **Get-AzDataLakeStoreAccount** ottiene i dettagli di un account di archivio dati per i laghi.</span><span class="sxs-lookup"><span data-stu-id="55759-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="55759-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55759-110">EXAMPLES</span></span>

### <span data-ttu-id="55759-111">Esempio 1: ottenere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="55759-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="55759-112">Questo comando consente di ottenere l'account denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="55759-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="55759-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55759-113">PARAMETERS</span></span>

### <span data-ttu-id="55759-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55759-114">-DefaultProfile</span></span>
<span data-ttu-id="55759-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="55759-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55759-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="55759-116">-Name</span></span>
<span data-ttu-id="55759-117">Specifica il nome dell'account da ottenere.</span><span class="sxs-lookup"><span data-stu-id="55759-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="55759-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55759-118">-ResourceGroupName</span></span>
<span data-ttu-id="55759-119">Specifica il nome del gruppo di risorse che contiene l'account di data Lake Store da ottenere.</span><span class="sxs-lookup"><span data-stu-id="55759-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="55759-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55759-120">CommonParameters</span></span>
<span data-ttu-id="55759-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55759-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55759-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55759-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55759-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55759-123">INPUTS</span></span>

### <span data-ttu-id="55759-124">System. String</span><span class="sxs-lookup"><span data-stu-id="55759-124">System.String</span></span>

## <span data-ttu-id="55759-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55759-125">OUTPUTS</span></span>

### <span data-ttu-id="55759-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="55759-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="55759-127">Note</span><span class="sxs-lookup"><span data-stu-id="55759-127">NOTES</span></span>

## <span data-ttu-id="55759-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55759-128">RELATED LINKS</span></span>

[<span data-ttu-id="55759-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="55759-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="55759-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="55759-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="55759-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="55759-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="55759-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="55759-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


