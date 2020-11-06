---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 8aeb682b270de821a6944c619d7933148b2855e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521697"
---
# <span data-ttu-id="825b5-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="825b5-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="825b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="825b5-102">SYNOPSIS</span></span>
<span data-ttu-id="825b5-103">Verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="825b5-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="825b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="825b5-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="825b5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="825b5-105">DESCRIPTION</span></span>
<span data-ttu-id="825b5-106">Il cmdlet **test-AzureRmDataLakeStoreAccount** verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="825b5-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="825b5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="825b5-107">EXAMPLES</span></span>

### <span data-ttu-id="825b5-108">Esempio 1: testare un account</span><span class="sxs-lookup"><span data-stu-id="825b5-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="825b5-109">Questo comando verifica se l'account denominato ContosoADL esiste.</span><span class="sxs-lookup"><span data-stu-id="825b5-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="825b5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="825b5-110">PARAMETERS</span></span>

### <span data-ttu-id="825b5-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="825b5-111">-Name</span></span>
<span data-ttu-id="825b5-112">Specifica il nome dell'account di data Lake Store da testare.</span><span class="sxs-lookup"><span data-stu-id="825b5-112">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="825b5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="825b5-113">-ResourceGroupName</span></span>
<span data-ttu-id="825b5-114">Specifica il nome del gruppo di risorse che contiene l'account da testare.</span><span class="sxs-lookup"><span data-stu-id="825b5-114">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="825b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825b5-115">-DefaultProfile</span></span>
<span data-ttu-id="825b5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="825b5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="825b5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825b5-117">CommonParameters</span></span>
<span data-ttu-id="825b5-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="825b5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825b5-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="825b5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825b5-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="825b5-120">INPUTS</span></span>

## <span data-ttu-id="825b5-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="825b5-121">OUTPUTS</span></span>

### <span data-ttu-id="825b5-122">bool</span><span class="sxs-lookup"><span data-stu-id="825b5-122">bool</span></span>
<span data-ttu-id="825b5-123">Vero o falso che indica l'esistenza dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="825b5-123">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="825b5-124">Note</span><span class="sxs-lookup"><span data-stu-id="825b5-124">NOTES</span></span>

## <span data-ttu-id="825b5-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="825b5-125">RELATED LINKS</span></span>

[<span data-ttu-id="825b5-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="825b5-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="825b5-127">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="825b5-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="825b5-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="825b5-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="825b5-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="825b5-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


