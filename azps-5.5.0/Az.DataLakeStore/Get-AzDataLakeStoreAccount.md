---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188598"
---
# <span data-ttu-id="63c2a-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="63c2a-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="63c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="63c2a-103">Recupera i dettagli di un account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="63c2a-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="63c2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63c2a-104">SYNTAX</span></span>

### <span data-ttu-id="63c2a-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63c2a-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63c2a-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="63c2a-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63c2a-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="63c2a-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63c2a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63c2a-108">DESCRIPTION</span></span>
<span data-ttu-id="63c2a-109">Il cmdlet **Get-AzDataLakeStoreAccount** ottiene i dettagli di un account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="63c2a-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="63c2a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63c2a-110">EXAMPLES</span></span>

### <span data-ttu-id="63c2a-111">Esempio 1: Ottenere un account Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="63c2a-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="63c2a-112">Questo comando recupera l'account denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="63c2a-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="63c2a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63c2a-113">PARAMETERS</span></span>

### <span data-ttu-id="63c2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c2a-114">-DefaultProfile</span></span>
<span data-ttu-id="63c2a-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="63c2a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63c2a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="63c2a-116">-Name</span></span>
<span data-ttu-id="63c2a-117">Specifica il nome dell'account da ottenere.</span><span class="sxs-lookup"><span data-stu-id="63c2a-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="63c2a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63c2a-118">-ResourceGroupName</span></span>
<span data-ttu-id="63c2a-119">Specifica il nome del gruppo di risorse che contiene l'account Data Lake Store da ottenere.</span><span class="sxs-lookup"><span data-stu-id="63c2a-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="63c2a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c2a-120">CommonParameters</span></span>
<span data-ttu-id="63c2a-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63c2a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c2a-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63c2a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c2a-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="63c2a-123">INPUTS</span></span>

### <span data-ttu-id="63c2a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="63c2a-124">System.String</span></span>

## <span data-ttu-id="63c2a-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63c2a-125">OUTPUTS</span></span>

### <span data-ttu-id="63c2a-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="63c2a-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="63c2a-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="63c2a-127">NOTES</span></span>

## <span data-ttu-id="63c2a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63c2a-128">RELATED LINKS</span></span>

[<span data-ttu-id="63c2a-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="63c2a-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="63c2a-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="63c2a-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="63c2a-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="63c2a-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="63c2a-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="63c2a-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


