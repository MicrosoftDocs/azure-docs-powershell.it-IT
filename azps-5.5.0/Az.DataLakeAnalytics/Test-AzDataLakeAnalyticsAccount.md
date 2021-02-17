---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 0f0cad155cdb274596aba449e26e82b94ca56aae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198151"
---
# <span data-ttu-id="cd0ad-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="cd0ad-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="cd0ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd0ad-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0ad-103">Verifica l'esistenza di un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cd0ad-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="cd0ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd0ad-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd0ad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd0ad-105">DESCRIPTION</span></span>
<span data-ttu-id="cd0ad-106">Il cmdlet **Test-AzDataLakeAnalyticsAccount** verifica l'esistenza di un account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cd0ad-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="cd0ad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd0ad-107">EXAMPLES</span></span>

### <span data-ttu-id="cd0ad-108">Esempio 1: Verificare l'esistenza di un account</span><span class="sxs-lookup"><span data-stu-id="cd0ad-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="cd0ad-109">Questo comando verifica l'esistenza dell'account denominato ContosoAdlAccount.</span><span class="sxs-lookup"><span data-stu-id="cd0ad-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="cd0ad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd0ad-110">PARAMETERS</span></span>

### <span data-ttu-id="cd0ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd0ad-111">-DefaultProfile</span></span>
<span data-ttu-id="cd0ad-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="cd0ad-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd0ad-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cd0ad-113">-Name</span></span>
<span data-ttu-id="cd0ad-114">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cd0ad-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="cd0ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd0ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="cd0ad-116">Specifica il nome del gruppo di risorse dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cd0ad-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="cd0ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0ad-117">CommonParameters</span></span>
<span data-ttu-id="cd0ad-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd0ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0ad-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd0ad-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0ad-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd0ad-120">INPUTS</span></span>

### <span data-ttu-id="cd0ad-121">System.String</span><span class="sxs-lookup"><span data-stu-id="cd0ad-121">System.String</span></span>

## <span data-ttu-id="cd0ad-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd0ad-122">OUTPUTS</span></span>

### <span data-ttu-id="cd0ad-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd0ad-123">System.Boolean</span></span>

## <span data-ttu-id="cd0ad-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd0ad-124">NOTES</span></span>

## <span data-ttu-id="cd0ad-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd0ad-125">RELATED LINKS</span></span>

[<span data-ttu-id="cd0ad-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="cd0ad-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="cd0ad-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="cd0ad-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="cd0ad-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="cd0ad-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


