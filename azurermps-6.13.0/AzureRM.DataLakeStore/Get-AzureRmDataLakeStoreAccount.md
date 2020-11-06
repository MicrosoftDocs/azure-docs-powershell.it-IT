---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507511"
---
# <span data-ttu-id="71e45-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71e45-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="71e45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71e45-102">SYNOPSIS</span></span>
<span data-ttu-id="71e45-103">Ottiene i dettagli di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71e45-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71e45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71e45-104">SYNTAX</span></span>

### <span data-ttu-id="71e45-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71e45-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71e45-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71e45-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71e45-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="71e45-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e45-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71e45-108">DESCRIPTION</span></span>
<span data-ttu-id="71e45-109">Il cmdlet **Get-AzureRmDataLakeStoreAccount** ottiene i dettagli di un account di archivio dati per i laghi.</span><span class="sxs-lookup"><span data-stu-id="71e45-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="71e45-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71e45-110">EXAMPLES</span></span>

### <span data-ttu-id="71e45-111">Esempio 1: ottenere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="71e45-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="71e45-112">Questo comando consente di ottenere l'account denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="71e45-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="71e45-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71e45-113">PARAMETERS</span></span>

### <span data-ttu-id="71e45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e45-114">-DefaultProfile</span></span>
<span data-ttu-id="71e45-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="71e45-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71e45-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="71e45-116">-Name</span></span>
<span data-ttu-id="71e45-117">Specifica il nome dell'account da ottenere.</span><span class="sxs-lookup"><span data-stu-id="71e45-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="71e45-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e45-118">-ResourceGroupName</span></span>
<span data-ttu-id="71e45-119">Specifica il nome del gruppo di risorse che contiene l'account di data Lake Store da ottenere.</span><span class="sxs-lookup"><span data-stu-id="71e45-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="71e45-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e45-120">CommonParameters</span></span>
<span data-ttu-id="71e45-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e45-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e45-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e45-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e45-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71e45-123">INPUTS</span></span>

### <span data-ttu-id="71e45-124">System. String</span><span class="sxs-lookup"><span data-stu-id="71e45-124">System.String</span></span>

## <span data-ttu-id="71e45-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71e45-125">OUTPUTS</span></span>

### <span data-ttu-id="71e45-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71e45-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="71e45-127">Note</span><span class="sxs-lookup"><span data-stu-id="71e45-127">NOTES</span></span>

## <span data-ttu-id="71e45-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71e45-128">RELATED LINKS</span></span>

[<span data-ttu-id="71e45-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71e45-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="71e45-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71e45-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="71e45-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71e45-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="71e45-132">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="71e45-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


