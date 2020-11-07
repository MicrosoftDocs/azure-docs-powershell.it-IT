---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865494"
---
# <span data-ttu-id="4d2ed-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d2ed-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="4d2ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d2ed-102">SYNOPSIS</span></span>
<span data-ttu-id="4d2ed-103">Verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="4d2ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d2ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d2ed-105">DESCRIPTION</span></span>
<span data-ttu-id="4d2ed-106">Il cmdlet **test-AzDataLakeStoreAccount** verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="4d2ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-107">EXAMPLES</span></span>

### <span data-ttu-id="4d2ed-108">Esempio 1: testare un account</span><span class="sxs-lookup"><span data-stu-id="4d2ed-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="4d2ed-109">Questo comando verifica se l'account denominato ContosoADL esiste.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="4d2ed-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-110">PARAMETERS</span></span>

### <span data-ttu-id="4d2ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d2ed-111">-DefaultProfile</span></span>
<span data-ttu-id="4d2ed-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4d2ed-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d2ed-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d2ed-113">-Name</span></span>
<span data-ttu-id="4d2ed-114">Specifica il nome dell'account di data Lake Store da testare.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="4d2ed-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d2ed-115">-ResourceGroupName</span></span>
<span data-ttu-id="4d2ed-116">Specifica il nome del gruppo di risorse che contiene l'account da testare.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="4d2ed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d2ed-117">CommonParameters</span></span>
<span data-ttu-id="4d2ed-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d2ed-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d2ed-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d2ed-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-120">INPUTS</span></span>

### <span data-ttu-id="4d2ed-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4d2ed-121">System.String</span></span>

## <span data-ttu-id="4d2ed-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d2ed-122">OUTPUTS</span></span>

### <span data-ttu-id="4d2ed-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d2ed-123">System.Boolean</span></span>

## <span data-ttu-id="4d2ed-124">Note</span><span class="sxs-lookup"><span data-stu-id="4d2ed-124">NOTES</span></span>

## <span data-ttu-id="4d2ed-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-125">RELATED LINKS</span></span>

[<span data-ttu-id="4d2ed-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d2ed-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4d2ed-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d2ed-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4d2ed-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d2ed-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="4d2ed-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d2ed-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


