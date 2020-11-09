---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297708"
---
# <span data-ttu-id="fc111-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fc111-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="fc111-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc111-102">SYNOPSIS</span></span>
<span data-ttu-id="fc111-103">Verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc111-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="fc111-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc111-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc111-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc111-105">DESCRIPTION</span></span>
<span data-ttu-id="fc111-106">Il cmdlet **test-AzDataLakeStoreAccount** verifica l'esistenza di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc111-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="fc111-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc111-107">EXAMPLES</span></span>

### <span data-ttu-id="fc111-108">Esempio 1: testare un account</span><span class="sxs-lookup"><span data-stu-id="fc111-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="fc111-109">Questo comando verifica se l'account denominato ContosoADL esiste.</span><span class="sxs-lookup"><span data-stu-id="fc111-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="fc111-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc111-110">PARAMETERS</span></span>

### <span data-ttu-id="fc111-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc111-111">-DefaultProfile</span></span>
<span data-ttu-id="fc111-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fc111-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc111-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc111-113">-Name</span></span>
<span data-ttu-id="fc111-114">Specifica il nome dell'account di data Lake Store da testare.</span><span class="sxs-lookup"><span data-stu-id="fc111-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="fc111-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc111-115">-ResourceGroupName</span></span>
<span data-ttu-id="fc111-116">Specifica il nome del gruppo di risorse che contiene l'account da testare.</span><span class="sxs-lookup"><span data-stu-id="fc111-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="fc111-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc111-117">CommonParameters</span></span>
<span data-ttu-id="fc111-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc111-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc111-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc111-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc111-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc111-120">INPUTS</span></span>

### <span data-ttu-id="fc111-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fc111-121">System.String</span></span>

## <span data-ttu-id="fc111-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc111-122">OUTPUTS</span></span>

### <span data-ttu-id="fc111-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc111-123">System.Boolean</span></span>

## <span data-ttu-id="fc111-124">Note</span><span class="sxs-lookup"><span data-stu-id="fc111-124">NOTES</span></span>

## <span data-ttu-id="fc111-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc111-125">RELATED LINKS</span></span>

[<span data-ttu-id="fc111-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fc111-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="fc111-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fc111-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="fc111-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fc111-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="fc111-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="fc111-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


