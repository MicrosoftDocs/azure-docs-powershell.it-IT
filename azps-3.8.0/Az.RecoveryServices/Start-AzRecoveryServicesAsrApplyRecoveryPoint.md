---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: b06501fafbc573e10ac7d5dba3435dbf96342ba0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410736"
---
# <span data-ttu-id="901a3-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="901a3-101">Start-AzRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="901a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="901a3-102">SYNOPSIS</span></span>
<span data-ttu-id="901a3-103">Modifica un punto di ripristino per un elemento protetto con errore prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="901a3-103">Changes a recovery point for a failed over protected item before committing the failover operation.</span></span>

## <span data-ttu-id="901a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="901a3-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="901a3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="901a3-105">DESCRIPTION</span></span>
<span data-ttu-id="901a3-106">**Start-AzRecoveryServicesAsrApplyRecoveryPoint** cambia il punto di ripristino per un elemento protetto con failover prima di eseguire il commit dell'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="901a3-106">The **Start-AzRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="901a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="901a3-107">EXAMPLES</span></span>

### <span data-ttu-id="901a3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="901a3-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="901a3-109">Avvia l'applicazione del punto di ripristino specificato all'elemento protetto da replica e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="901a3-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="901a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="901a3-110">PARAMETERS</span></span>

### <span data-ttu-id="901a3-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="901a3-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="901a3-112">Specifica il file del certificato primario se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="901a3-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="901a3-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="901a3-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="901a3-114">Specifica il file del certificato secondario se viene usata la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="901a3-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="901a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901a3-115">-DefaultProfile</span></span>
<span data-ttu-id="901a3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="901a3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="901a3-117">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="901a3-117">-RecoveryPoint</span></span>
<span data-ttu-id="901a3-118">Specifica l'oggetto punto di ripristino corrispondente al punto di ripristino da applicare.</span><span class="sxs-lookup"><span data-stu-id="901a3-118">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901a3-119">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="901a3-119">-ReplicationProtectedItem</span></span>
<span data-ttu-id="901a3-120">Specifica l'oggetto elemento protetto da replica ASR.</span><span class="sxs-lookup"><span data-stu-id="901a3-120">Specifies the ASR replication protected item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="901a3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="901a3-121">-Confirm</span></span>
<span data-ttu-id="901a3-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="901a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="901a3-123">-WhatIf</span></span>
<span data-ttu-id="901a3-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="901a3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="901a3-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="901a3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901a3-126">CommonParameters</span></span>
<span data-ttu-id="901a3-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901a3-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="901a3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901a3-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="901a3-129">INPUTS</span></span>

### <span data-ttu-id="901a3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="901a3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="901a3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="901a3-131">OUTPUTS</span></span>

### <span data-ttu-id="901a3-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="901a3-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="901a3-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="901a3-133">NOTES</span></span>

## <span data-ttu-id="901a3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="901a3-134">RELATED LINKS</span></span>


