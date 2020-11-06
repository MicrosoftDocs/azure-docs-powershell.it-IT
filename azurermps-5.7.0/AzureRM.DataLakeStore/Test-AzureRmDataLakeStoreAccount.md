---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 15c0614094ed28a9888e2e39a6cfb81547fbb6e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520470"
---
# <span data-ttu-id="05f8b-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05f8b-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="05f8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="05f8b-103">Verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="05f8b-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05f8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05f8b-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05f8b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="05f8b-106">Il cmdlet **test-AzureRmDataLakeStoreAccount** verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="05f8b-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="05f8b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="05f8b-108">Esempio 1: testare un account</span><span class="sxs-lookup"><span data-stu-id="05f8b-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="05f8b-109">Questo comando verifica se l'account denominato ContosoADL esiste.</span><span class="sxs-lookup"><span data-stu-id="05f8b-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="05f8b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05f8b-110">PARAMETERS</span></span>

### <span data-ttu-id="05f8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f8b-111">-DefaultProfile</span></span>
<span data-ttu-id="05f8b-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="05f8b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05f8b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="05f8b-113">-Name</span></span>
<span data-ttu-id="05f8b-114">Specifica il nome dell'account di data Lake Store da testare.</span><span class="sxs-lookup"><span data-stu-id="05f8b-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05f8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="05f8b-116">Specifica il nome del gruppo di risorse che contiene l'account da testare.</span><span class="sxs-lookup"><span data-stu-id="05f8b-116">Specifies the name of the resource group that contains the account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05f8b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f8b-117">CommonParameters</span></span>
<span data-ttu-id="05f8b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05f8b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f8b-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05f8b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f8b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05f8b-120">INPUTS</span></span>

### <span data-ttu-id="05f8b-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="05f8b-121">None</span></span>
<span data-ttu-id="05f8b-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="05f8b-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05f8b-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05f8b-123">OUTPUTS</span></span>

### <span data-ttu-id="05f8b-124">bool</span><span class="sxs-lookup"><span data-stu-id="05f8b-124">bool</span></span>
<span data-ttu-id="05f8b-125">Vero o falso che indica l'esistenza dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="05f8b-125">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="05f8b-126">Note</span><span class="sxs-lookup"><span data-stu-id="05f8b-126">NOTES</span></span>

## <span data-ttu-id="05f8b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05f8b-127">RELATED LINKS</span></span>

[<span data-ttu-id="05f8b-128">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05f8b-128">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="05f8b-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05f8b-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="05f8b-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05f8b-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="05f8b-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="05f8b-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


