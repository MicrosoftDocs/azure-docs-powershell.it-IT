---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 845fbb645ca9ba3495aa0dcf2b56cdbd793630e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963101"
---
# <span data-ttu-id="c1c34-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1c34-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="c1c34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c34-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c34-103">Recupera i dettagli di un account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c1c34-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="c1c34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1c34-104">SYNTAX</span></span>

### <span data-ttu-id="c1c34-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1c34-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1c34-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1c34-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1c34-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="c1c34-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1c34-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c1c34-108">DESCRIPTION</span></span>
<span data-ttu-id="c1c34-109">Il cmdlet **Get-AzDataLakeStoreAccount** ottiene i dettagli di un account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c1c34-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="c1c34-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1c34-110">EXAMPLES</span></span>

### <span data-ttu-id="c1c34-111">Esempio 1: Ottenere un account Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c1c34-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="c1c34-112">Questo comando recupera l'account denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="c1c34-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="c1c34-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1c34-113">PARAMETERS</span></span>

### <span data-ttu-id="c1c34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c34-114">-DefaultProfile</span></span>
<span data-ttu-id="c1c34-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c1c34-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1c34-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c1c34-116">-Name</span></span>
<span data-ttu-id="c1c34-117">Specifica il nome dell'account da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c1c34-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="c1c34-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c34-118">-ResourceGroupName</span></span>
<span data-ttu-id="c1c34-119">Specifica il nome del gruppo di risorse che contiene l'account Data Lake Store da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c1c34-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="c1c34-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c34-120">CommonParameters</span></span>
<span data-ttu-id="c1c34-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c34-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c34-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c34-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c34-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="c1c34-123">INPUTS</span></span>

### <span data-ttu-id="c1c34-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c1c34-124">System.String</span></span>

## <span data-ttu-id="c1c34-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1c34-125">OUTPUTS</span></span>

### <span data-ttu-id="c1c34-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1c34-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="c1c34-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="c1c34-127">NOTES</span></span>

## <span data-ttu-id="c1c34-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1c34-128">RELATED LINKS</span></span>

[<span data-ttu-id="c1c34-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1c34-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c1c34-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1c34-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c1c34-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1c34-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c1c34-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c1c34-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


