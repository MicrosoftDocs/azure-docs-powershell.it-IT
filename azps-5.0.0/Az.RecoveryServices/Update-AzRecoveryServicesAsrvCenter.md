---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202630"
---
# <span data-ttu-id="091ba-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="091ba-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="091ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="091ba-102">SYNOPSIS</span></span>
<span data-ttu-id="091ba-103">Aggiornare i dettagli dell'individuazione per un vCenter registrato.</span><span class="sxs-lookup"><span data-stu-id="091ba-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="091ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="091ba-104">SYNTAX</span></span>

### <span data-ttu-id="091ba-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="091ba-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="091ba-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="091ba-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="091ba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="091ba-107">DESCRIPTION</span></span>
<span data-ttu-id="091ba-108">Il cmdlet **Update-AzRecoveryServicesAsrvCenter** aggiorna i dettagli dell'individuazione per un vCenter registrato.</span><span class="sxs-lookup"><span data-stu-id="091ba-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="091ba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="091ba-109">EXAMPLES</span></span>

### <span data-ttu-id="091ba-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="091ba-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="091ba-111">Aggiornare i dettagli dell'individuazione per un vCenter registrato.</span><span class="sxs-lookup"><span data-stu-id="091ba-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="091ba-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="091ba-112">PARAMETERS</span></span>

### <span data-ttu-id="091ba-113">-Account</span><span class="sxs-lookup"><span data-stu-id="091ba-113">-Account</span></span>
<span data-ttu-id="091ba-114">account delle credenziali di accesso vCenter.</span><span class="sxs-lookup"><span data-stu-id="091ba-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="091ba-115">-DefaultProfile</span></span>
<span data-ttu-id="091ba-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="091ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="091ba-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="091ba-117">-InputObject</span></span>
<span data-ttu-id="091ba-118">L'oggetto vCenter Server per aggiornare i dettagli dell'individuazione.</span><span class="sxs-lookup"><span data-stu-id="091ba-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="091ba-119">-Porta</span><span class="sxs-lookup"><span data-stu-id="091ba-119">-Port</span></span>
<span data-ttu-id="091ba-120">Porta TCP sul server vCenter da usare per l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="091ba-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="091ba-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="091ba-121">-ResourceId</span></span>
<span data-ttu-id="091ba-122">Specifica il resourceId di vCenter.</span><span class="sxs-lookup"><span data-stu-id="091ba-122">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="091ba-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="091ba-123">-Confirm</span></span>
<span data-ttu-id="091ba-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="091ba-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="091ba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="091ba-125">-WhatIf</span></span>
<span data-ttu-id="091ba-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="091ba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="091ba-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="091ba-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="091ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091ba-128">CommonParameters</span></span>
<span data-ttu-id="091ba-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="091ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091ba-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="091ba-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091ba-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="091ba-131">INPUTS</span></span>

### <span data-ttu-id="091ba-132">System. String</span><span class="sxs-lookup"><span data-stu-id="091ba-132">System.String</span></span>

### <span data-ttu-id="091ba-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="091ba-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="091ba-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="091ba-134">OUTPUTS</span></span>

### <span data-ttu-id="091ba-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="091ba-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="091ba-136">Note</span><span class="sxs-lookup"><span data-stu-id="091ba-136">NOTES</span></span>

## <span data-ttu-id="091ba-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="091ba-137">RELATED LINKS</span></span>
