---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032841"
---
# <span data-ttu-id="6129a-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6129a-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="6129a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6129a-102">SYNOPSIS</span></span>
<span data-ttu-id="6129a-103">Ottiene un piano di ripristino o tutti i piani di ripristino nel Vault di servizi di ripristino</span><span class="sxs-lookup"><span data-stu-id="6129a-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="6129a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6129a-104">SYNTAX</span></span>

### <span data-ttu-id="6129a-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6129a-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6129a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6129a-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6129a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6129a-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6129a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6129a-108">DESCRIPTION</span></span>
<span data-ttu-id="6129a-109">Il cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan** consente di ottenere i dettagli del piano di ripristino specificato o di tutti i piani di ripristino nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6129a-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="6129a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6129a-110">EXAMPLES</span></span>

### <span data-ttu-id="6129a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6129a-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="6129a-112">Ottiene il piano di ripristino con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6129a-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="6129a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6129a-113">PARAMETERS</span></span>

### <span data-ttu-id="6129a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6129a-114">-DefaultProfile</span></span>
<span data-ttu-id="6129a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6129a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6129a-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6129a-116">-FriendlyName</span></span>
<span data-ttu-id="6129a-117">Specifica il nome descrittivo del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6129a-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6129a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6129a-118">-Name</span></span>
<span data-ttu-id="6129a-119">Specifica il nome del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6129a-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6129a-120">-Path</span><span class="sxs-lookup"><span data-stu-id="6129a-120">-Path</span></span>
<span data-ttu-id="6129a-121">Specifica il percorso del file a cui questo cmdlet salva la definizione JSON del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6129a-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="6129a-122">La definizione JSON può essere modificata per modificare il piano di ripristino e usato per aggiornare il piano di ripristino tramite il cmdlet Update-AzRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6129a-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6129a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6129a-123">CommonParameters</span></span>
<span data-ttu-id="6129a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6129a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6129a-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6129a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6129a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6129a-126">INPUTS</span></span>

### <span data-ttu-id="6129a-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6129a-127">None</span></span>

## <span data-ttu-id="6129a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6129a-128">OUTPUTS</span></span>

### <span data-ttu-id="6129a-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6129a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="6129a-130">Note</span><span class="sxs-lookup"><span data-stu-id="6129a-130">NOTES</span></span>

## <span data-ttu-id="6129a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6129a-131">RELATED LINKS</span></span>

[<span data-ttu-id="6129a-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6129a-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6129a-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6129a-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="6129a-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6129a-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
