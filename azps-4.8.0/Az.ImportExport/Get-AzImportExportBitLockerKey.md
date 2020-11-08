---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190709"
---
# <span data-ttu-id="f850e-101">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="f850e-101">Get-AzImportExportBitLockerKey</span></span>

## <span data-ttu-id="f850e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f850e-102">SYNOPSIS</span></span>
<span data-ttu-id="f850e-103">Restituisce le chiavi di BitLocker per tutte le unità nel processo specificato.</span><span class="sxs-lookup"><span data-stu-id="f850e-103">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="f850e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f850e-104">SYNTAX</span></span>

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f850e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f850e-105">DESCRIPTION</span></span>
<span data-ttu-id="f850e-106">Restituisce le chiavi di BitLocker per tutte le unità nel processo specificato.</span><span class="sxs-lookup"><span data-stu-id="f850e-106">Returns the BitLocker Keys for all drives in the specified job.</span></span>

## <span data-ttu-id="f850e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f850e-107">EXAMPLES</span></span>

### <span data-ttu-id="f850e-108">Esempio 1: elencare tutte le chiavi di BitLocker nel processo di ImportExport specificato</span><span class="sxs-lookup"><span data-stu-id="f850e-108">Example 1: List all BitLocker Keys in specified ImportExport job</span></span>
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

<span data-ttu-id="f850e-109">Questo cmdlet elenca tutte le chiavi di BitLocker in un processo di ImportExport specificato.</span><span class="sxs-lookup"><span data-stu-id="f850e-109">This cmdlet lists all BitLocker Keys in specified ImportExport job.</span></span>

## <span data-ttu-id="f850e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f850e-110">PARAMETERS</span></span>

### <span data-ttu-id="f850e-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="f850e-111">-AcceptLanguage</span></span>
<span data-ttu-id="f850e-112">Specifica la lingua preferita per la risposta.</span><span class="sxs-lookup"><span data-stu-id="f850e-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="f850e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f850e-113">-DefaultProfile</span></span>
<span data-ttu-id="f850e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f850e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f850e-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="f850e-115">-JobName</span></span>
<span data-ttu-id="f850e-116">Nome del processo di importazione/esportazione.</span><span class="sxs-lookup"><span data-stu-id="f850e-116">The name of the import/export job.</span></span>

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

### <span data-ttu-id="f850e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f850e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f850e-118">Il nome del gruppo di risorse identifica in modo univoco il gruppo di risorse nell'abbonamento utente.</span><span class="sxs-lookup"><span data-stu-id="f850e-118">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="f850e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f850e-119">-SubscriptionId</span></span>
<span data-ttu-id="f850e-120">ID sottoscrizione per l'utente di Azure.</span><span class="sxs-lookup"><span data-stu-id="f850e-120">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="f850e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f850e-121">CommonParameters</span></span>
<span data-ttu-id="f850e-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f850e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f850e-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f850e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f850e-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f850e-124">INPUTS</span></span>

## <span data-ttu-id="f850e-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f850e-125">OUTPUTS</span></span>

### <span data-ttu-id="f850e-126">Microsoft. Azure. PowerShell. Cmdlets. ImportExport. Models. Api20161101. IDriveBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="f850e-126">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey</span></span>

## <span data-ttu-id="f850e-127">Note</span><span class="sxs-lookup"><span data-stu-id="f850e-127">NOTES</span></span>

<span data-ttu-id="f850e-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f850e-128">ALIASES</span></span>

## <span data-ttu-id="f850e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f850e-129">RELATED LINKS</span></span>

