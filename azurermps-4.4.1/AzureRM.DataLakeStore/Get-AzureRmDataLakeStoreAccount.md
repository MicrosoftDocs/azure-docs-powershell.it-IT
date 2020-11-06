---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510635"
---
# <span data-ttu-id="c320e-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c320e-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="c320e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c320e-102">SYNOPSIS</span></span>
<span data-ttu-id="c320e-103">Ottiene i dettagli di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c320e-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c320e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c320e-104">SYNTAX</span></span>

### <span data-ttu-id="c320e-105">Tutti in abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c320e-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c320e-106">Tutti nel gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="c320e-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c320e-107">Account specifico</span><span class="sxs-lookup"><span data-stu-id="c320e-107">Specific Account</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c320e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c320e-108">DESCRIPTION</span></span>
<span data-ttu-id="c320e-109">Il cmdlet **Get-AzureRmDataLakeStoreAccount** ottiene i dettagli di un account di archivio dati per i laghi.</span><span class="sxs-lookup"><span data-stu-id="c320e-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="c320e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c320e-110">EXAMPLES</span></span>

### <span data-ttu-id="c320e-111">Esempio 1: ottenere un account di data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c320e-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="c320e-112">Questo comando consente di ottenere l'account denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="c320e-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="c320e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c320e-113">PARAMETERS</span></span>

### <span data-ttu-id="c320e-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="c320e-114">-Name</span></span>
<span data-ttu-id="c320e-115">Specifica il nome dell'account da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c320e-115">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c320e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c320e-116">-ResourceGroupName</span></span>
<span data-ttu-id="c320e-117">Specifica il nome del gruppo di risorse che contiene l'account di data Lake Store da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c320e-117">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c320e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c320e-118">-DefaultProfile</span></span>
<span data-ttu-id="c320e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c320e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c320e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c320e-120">CommonParameters</span></span>
<span data-ttu-id="c320e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c320e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c320e-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c320e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c320e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c320e-123">INPUTS</span></span>

## <span data-ttu-id="c320e-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c320e-124">OUTPUTS</span></span>

### <span data-ttu-id="c320e-125">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c320e-125">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="c320e-126">L'account specifico per i dati del lago Store richiesto.</span><span class="sxs-lookup"><span data-stu-id="c320e-126">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="c320e-127">Elenco<PSDataLakeStoreAccount></span><span class="sxs-lookup"><span data-stu-id="c320e-127">List<PSDataLakeStoreAccount></span></span>
<span data-ttu-id="c320e-128">Elenco di account di archiviazione dei dati del lago nel gruppo di risorse o nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="c320e-128">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="c320e-129">Note</span><span class="sxs-lookup"><span data-stu-id="c320e-129">NOTES</span></span>

## <span data-ttu-id="c320e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c320e-130">RELATED LINKS</span></span>

[<span data-ttu-id="c320e-131">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c320e-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c320e-132">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c320e-132">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c320e-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c320e-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="c320e-134">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c320e-134">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


