---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 77247853fe6412b0d01fb01c71e592efca12063d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674841"
---
# <span data-ttu-id="2157f-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2157f-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="2157f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2157f-102">SYNOPSIS</span></span>
<span data-ttu-id="2157f-103">Controlla l'esistenza di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="2157f-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="2157f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2157f-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2157f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2157f-105">DESCRIPTION</span></span>
<span data-ttu-id="2157f-106">Il cmdlet **test-AzDataLakeAnalyticsAccount** controlla l'esistenza di un account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="2157f-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="2157f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2157f-107">EXAMPLES</span></span>

### <span data-ttu-id="2157f-108">Esempio 1: verificare se un account esiste</span><span class="sxs-lookup"><span data-stu-id="2157f-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="2157f-109">Questo comando verifica se l'account denominato ContosoAdlAccount esiste.</span><span class="sxs-lookup"><span data-stu-id="2157f-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="2157f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2157f-110">PARAMETERS</span></span>

### <span data-ttu-id="2157f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2157f-111">-DefaultProfile</span></span>
<span data-ttu-id="2157f-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2157f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2157f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2157f-113">-Name</span></span>
<span data-ttu-id="2157f-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="2157f-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="2157f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2157f-115">-ResourceGroupName</span></span>
<span data-ttu-id="2157f-116">Specifica il nome del gruppo di risorse dell'account di analisi dei dati sul lago.</span><span class="sxs-lookup"><span data-stu-id="2157f-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="2157f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2157f-117">CommonParameters</span></span>
<span data-ttu-id="2157f-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2157f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2157f-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2157f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2157f-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2157f-120">INPUTS</span></span>

### <span data-ttu-id="2157f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="2157f-121">System.String</span></span>

## <span data-ttu-id="2157f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2157f-122">OUTPUTS</span></span>

### <span data-ttu-id="2157f-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2157f-123">System.Boolean</span></span>

## <span data-ttu-id="2157f-124">Note</span><span class="sxs-lookup"><span data-stu-id="2157f-124">NOTES</span></span>

## <span data-ttu-id="2157f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2157f-125">RELATED LINKS</span></span>

[<span data-ttu-id="2157f-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2157f-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2157f-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2157f-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="2157f-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="2157f-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


