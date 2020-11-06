---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 61899a50c857fc3e8852d362d5905b0ca2fedf6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518140"
---
# <span data-ttu-id="87665-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="87665-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="87665-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87665-102">SYNOPSIS</span></span>
<span data-ttu-id="87665-103">Ottiene i dettagli di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="87665-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87665-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87665-104">SYNTAX</span></span>

### <span data-ttu-id="87665-105">GetAllInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87665-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87665-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87665-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87665-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="87665-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87665-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87665-108">DESCRIPTION</span></span>
<span data-ttu-id="87665-109">Il cmdlet **Get-AzureRmDataLakeStoreAccount** ottiene i dettagli di un account di archivio dati per i laghi.</span><span class="sxs-lookup"><span data-stu-id="87665-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="87665-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87665-110">EXAMPLES</span></span>

### <span data-ttu-id="87665-111">Esempio 1: ottenere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="87665-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="87665-112">Questo comando consente di ottenere l'account denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="87665-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="87665-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87665-113">PARAMETERS</span></span>

### <span data-ttu-id="87665-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87665-114">-DefaultProfile</span></span>
<span data-ttu-id="87665-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="87665-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87665-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="87665-116">-Name</span></span>
<span data-ttu-id="87665-117">Specifica il nome dell'account da ottenere.</span><span class="sxs-lookup"><span data-stu-id="87665-117">Specifies the name of the account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87665-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87665-118">-ResourceGroupName</span></span>
<span data-ttu-id="87665-119">Specifica il nome del gruppo di risorse che contiene l'account di data Lake Store da ottenere.</span><span class="sxs-lookup"><span data-stu-id="87665-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87665-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87665-120">CommonParameters</span></span>
<span data-ttu-id="87665-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87665-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87665-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87665-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87665-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87665-123">INPUTS</span></span>

### <span data-ttu-id="87665-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="87665-124">None</span></span>
<span data-ttu-id="87665-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="87665-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87665-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87665-126">OUTPUTS</span></span>

### <span data-ttu-id="87665-127">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="87665-127">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="87665-128">L'account specifico per i dati del lago Store richiesto.</span><span class="sxs-lookup"><span data-stu-id="87665-128">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="87665-129">Elenco<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="87665-129">List<PSDataLakeStoreAccountBasic></span></span>
<span data-ttu-id="87665-130">Elenco di account di archiviazione dei dati del lago nel gruppo di risorse o nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="87665-130">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="87665-131">Note</span><span class="sxs-lookup"><span data-stu-id="87665-131">NOTES</span></span>

## <span data-ttu-id="87665-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87665-132">RELATED LINKS</span></span>

[<span data-ttu-id="87665-133">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="87665-133">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="87665-134">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="87665-134">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="87665-135">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="87665-135">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="87665-136">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="87665-136">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


