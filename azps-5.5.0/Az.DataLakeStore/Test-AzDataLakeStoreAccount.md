---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180894"
---
# <span data-ttu-id="690f2-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="690f2-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="690f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="690f2-102">SYNOPSIS</span></span>
<span data-ttu-id="690f2-103">Verifica la presenza di un account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="690f2-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="690f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="690f2-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="690f2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="690f2-105">DESCRIPTION</span></span>
<span data-ttu-id="690f2-106">Il **cmdlet Test-AzDataLakeStoreAccount** verifica l'esistenza di un account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="690f2-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="690f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="690f2-107">EXAMPLES</span></span>

### <span data-ttu-id="690f2-108">Esempio 1: Testare un account</span><span class="sxs-lookup"><span data-stu-id="690f2-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="690f2-109">Questo comando verifica l'esistenza dell'account denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="690f2-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="690f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="690f2-110">PARAMETERS</span></span>

### <span data-ttu-id="690f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690f2-111">-DefaultProfile</span></span>
<span data-ttu-id="690f2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="690f2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="690f2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="690f2-113">-Name</span></span>
<span data-ttu-id="690f2-114">Specifica il nome dell'account Data Lake Store da testare.</span><span class="sxs-lookup"><span data-stu-id="690f2-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="690f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="690f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="690f2-116">Specifica il nome del gruppo di risorse che contiene l'account da testare.</span><span class="sxs-lookup"><span data-stu-id="690f2-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="690f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690f2-117">CommonParameters</span></span>
<span data-ttu-id="690f2-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690f2-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690f2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690f2-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="690f2-120">INPUTS</span></span>

### <span data-ttu-id="690f2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="690f2-121">System.String</span></span>

## <span data-ttu-id="690f2-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="690f2-122">OUTPUTS</span></span>

### <span data-ttu-id="690f2-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="690f2-123">System.Boolean</span></span>

## <span data-ttu-id="690f2-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="690f2-124">NOTES</span></span>

## <span data-ttu-id="690f2-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="690f2-125">RELATED LINKS</span></span>

[<span data-ttu-id="690f2-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="690f2-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="690f2-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="690f2-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="690f2-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="690f2-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="690f2-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="690f2-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


