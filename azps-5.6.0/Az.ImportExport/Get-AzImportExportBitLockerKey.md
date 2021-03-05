---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: fefd529b00b88c20b3703e1bcecbbb88c72d52e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963005"
---
# <span data-ttu-id="da0d4-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="da0d4-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="da0d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="da0d4-103">Restituisce le chiavi BitLocker per tutte le unità nel processo specificato.</span><span class="sxs-lookup"><span data-stu-id="da0d4-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="da0d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da0d4-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="da0d4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da0d4-105">DESCRIPTION</span></span>
<span data-ttu-id="da0d4-106">Restituisce le chiavi BitLocker per tutte le unità nel processo specificato.</span><span class="sxs-lookup"><span data-stu-id="da0d4-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="da0d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da0d4-107">EXAMPLES</span></span>

### <span data-ttu-id="da0d4-108">Esempio 1: Elencare tutte le chiavi BitLocker nel processo importExport specificato</span><span class="sxs-lookup"><span data-stu-id="da0d4-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="da0d4-109">Questo cmdlet elenca tutte le chiavi BitLocker nel processo ImportExport specificato.</span><span class="sxs-lookup"><span data-stu-id="da0d4-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="da0d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da0d4-110">PARAMETERS</span></span>

### <span data-ttu-id="da0d4-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="da0d4-111">-AcceptLanguage</span></span>
<span data-ttu-id="da0d4-112">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="da0d4-112">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0d4-113">-DefaultProfile</span></span>
<span data-ttu-id="da0d4-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0d4-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="da0d4-115">-JobName</span></span>
<span data-ttu-id="da0d4-116">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="da0d4-116">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da0d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="da0d4-118">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="da0d4-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0d4-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da0d4-119">-SubscriptionId</span></span>
<span data-ttu-id="da0d4-120">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="da0d4-120">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0d4-121">CommonParameters</span></span>
<span data-ttu-id="da0d4-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da0d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0d4-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da0d4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0d4-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="da0d4-124">INPUTS</span></span>

## <span data-ttu-id="da0d4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da0d4-125">OUTPUTS</span></span>

### <span data-ttu-id="da0d4-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="da0d4-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="da0d4-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="da0d4-127">NOTES</span></span>

<span data-ttu-id="da0d4-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da0d4-128">ALIASES</span></span>

## <span data-ttu-id="da0d4-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da0d4-129">RELATED LINKS</span></span>

