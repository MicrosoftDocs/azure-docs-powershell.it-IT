---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b1b3a05b6f2d19ba350567c8793822d4129c5445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685434"
---
# <span data-ttu-id="f30ac-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f30ac-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="f30ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f30ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f30ac-103">Verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f30ac-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f30ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f30ac-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f30ac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f30ac-105">DESCRIPTION</span></span>
<span data-ttu-id="f30ac-106">Il cmdlet **test-AzureRmDataLakeStoreAccount** verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f30ac-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="f30ac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f30ac-107">EXAMPLES</span></span>

### <span data-ttu-id="f30ac-108">Esempio 1: testare un account</span><span class="sxs-lookup"><span data-stu-id="f30ac-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="f30ac-109">Questo comando verifica se l'account denominato ContosoADL esiste.</span><span class="sxs-lookup"><span data-stu-id="f30ac-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="f30ac-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f30ac-110">PARAMETERS</span></span>

### <span data-ttu-id="f30ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30ac-111">-DefaultProfile</span></span>
<span data-ttu-id="f30ac-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f30ac-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f30ac-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f30ac-113">-Name</span></span>
<span data-ttu-id="f30ac-114">Specifica il nome dell'account di data Lake Store da testare.</span><span class="sxs-lookup"><span data-stu-id="f30ac-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f30ac-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30ac-115">-ResourceGroupName</span></span>
<span data-ttu-id="f30ac-116">Specifica il nome del gruppo di risorse che contiene l'account da testare.</span><span class="sxs-lookup"><span data-stu-id="f30ac-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="f30ac-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30ac-117">CommonParameters</span></span>
<span data-ttu-id="f30ac-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f30ac-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30ac-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f30ac-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30ac-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f30ac-120">INPUTS</span></span>

### <span data-ttu-id="f30ac-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f30ac-121">System.String</span></span>

## <span data-ttu-id="f30ac-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f30ac-122">OUTPUTS</span></span>

### <span data-ttu-id="f30ac-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f30ac-123">System.Boolean</span></span>

## <span data-ttu-id="f30ac-124">Note</span><span class="sxs-lookup"><span data-stu-id="f30ac-124">NOTES</span></span>

## <span data-ttu-id="f30ac-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f30ac-125">RELATED LINKS</span></span>

[<span data-ttu-id="f30ac-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f30ac-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f30ac-127">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f30ac-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f30ac-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f30ac-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f30ac-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f30ac-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


