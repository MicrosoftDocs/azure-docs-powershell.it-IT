---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BA387784-DFF5-4801-93F3-386454040B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 594cb9af7c1afb82187003e3ddd7c085a254c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507923"
---
# <span data-ttu-id="73aa3-101">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73aa3-101">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="73aa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="73aa3-103">Aggiorna un piano di ripristino nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="73aa3-103">Updates a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73aa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73aa3-104">SYNTAX</span></span>

### <span data-ttu-id="73aa3-105">ByRPObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73aa3-105">ByRPObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73aa3-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="73aa3-106">ByRPFile</span></span>
```
Update-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73aa3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73aa3-107">DESCRIPTION</span></span>
<span data-ttu-id="73aa3-108">Il cmdlet **Update-AzureRmSiteRecoveryRecoveryPlan** aggiorna un piano di ripristino in Azure Site Recovery e lo pubblica.</span><span class="sxs-lookup"><span data-stu-id="73aa3-108">The **Update-AzureRmSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="73aa3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73aa3-109">EXAMPLES</span></span>

### <span data-ttu-id="73aa3-110">Esempio 1: aggiornare un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="73aa3-110">Example 1: Update a recovery plan</span></span>
```
PS C:\>Update-AzureRmSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="73aa3-111">Questo comando Aggiorna il piano di ripristino specificato e lo pubblica.</span><span class="sxs-lookup"><span data-stu-id="73aa3-111">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="73aa3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73aa3-112">PARAMETERS</span></span>

### <span data-ttu-id="73aa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73aa3-113">-DefaultProfile</span></span>
<span data-ttu-id="73aa3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73aa3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73aa3-115">-Path</span><span class="sxs-lookup"><span data-stu-id="73aa3-115">-Path</span></span>
<span data-ttu-id="73aa3-116">Specifica il percorso del file del piano di ripristino del piano di ripristino che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="73aa3-116">Specifies the path of the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73aa3-117">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73aa3-117">-RecoveryPlan</span></span>
<span data-ttu-id="73aa3-118">Specifica un piano di ripristino che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="73aa3-118">Specifies a recovery plan that this cmdlet updates.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73aa3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73aa3-119">CommonParameters</span></span>
<span data-ttu-id="73aa3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73aa3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73aa3-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73aa3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73aa3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73aa3-122">INPUTS</span></span>

### <span data-ttu-id="73aa3-123">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73aa3-123">ASRRecoveryPlan</span></span>
<span data-ttu-id="73aa3-124">Il parametro ' RecoveryPlan ' accetta il valore di tipo ' ASRRecoveryPlan ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="73aa3-124">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="73aa3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73aa3-125">OUTPUTS</span></span>

## <span data-ttu-id="73aa3-126">Note</span><span class="sxs-lookup"><span data-stu-id="73aa3-126">NOTES</span></span>

## <span data-ttu-id="73aa3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73aa3-127">RELATED LINKS</span></span>

[<span data-ttu-id="73aa3-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73aa3-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="73aa3-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73aa3-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="73aa3-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73aa3-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)


