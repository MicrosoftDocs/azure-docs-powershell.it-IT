---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 298443c4b962a2be6c5cf3849657d0fe8bbaf978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509667"
---
# <span data-ttu-id="51865-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="51865-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="51865-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51865-102">SYNOPSIS</span></span>
<span data-ttu-id="51865-103">Aggiornare i dettagli dell'individuazione per un vCenter registrato.</span><span class="sxs-lookup"><span data-stu-id="51865-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51865-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51865-104">SYNTAX</span></span>

### <span data-ttu-id="51865-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51865-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51865-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51865-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51865-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51865-107">DESCRIPTION</span></span>
<span data-ttu-id="51865-108">Il cmdlet **Update-AzureRmRecoveryServicesAsrvCenter** aggiorna i dettagli dell'individuazione per un vCenter registrato.</span><span class="sxs-lookup"><span data-stu-id="51865-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="51865-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51865-109">EXAMPLES</span></span>

### <span data-ttu-id="51865-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51865-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="51865-111">Aggiornare i dettagli dell'individuazione per un vCenter registrato.</span><span class="sxs-lookup"><span data-stu-id="51865-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="51865-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51865-112">PARAMETERS</span></span>

### <span data-ttu-id="51865-113">-Account</span><span class="sxs-lookup"><span data-stu-id="51865-113">-Account</span></span>
<span data-ttu-id="51865-114">account delle credenziali di accesso vCenter.</span><span class="sxs-lookup"><span data-stu-id="51865-114">vCenter login credentials account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51865-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51865-115">-Confirm</span></span>
<span data-ttu-id="51865-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51865-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51865-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51865-117">-DefaultProfile</span></span>
<span data-ttu-id="51865-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51865-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51865-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51865-119">-InputObject</span></span>
<span data-ttu-id="51865-120">L'oggetto vCenter Server per aggiornare i dettagli dell'individuazione.</span><span class="sxs-lookup"><span data-stu-id="51865-120">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51865-121">-Porta</span><span class="sxs-lookup"><span data-stu-id="51865-121">-Port</span></span>
<span data-ttu-id="51865-122">Porta TCP sul server vCenter da usare per l'individuazione.</span><span class="sxs-lookup"><span data-stu-id="51865-122">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51865-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51865-123">-ResourceId</span></span>
<span data-ttu-id="51865-124">Specifica il resourceId di vCenter.</span><span class="sxs-lookup"><span data-stu-id="51865-124">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51865-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51865-125">-WhatIf</span></span>
<span data-ttu-id="51865-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51865-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51865-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51865-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51865-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51865-128">CommonParameters</span></span>
<span data-ttu-id="51865-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51865-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51865-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51865-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51865-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51865-131">INPUTS</span></span>

### <span data-ttu-id="51865-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="51865-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="51865-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51865-133">OUTPUTS</span></span>

### <span data-ttu-id="51865-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="51865-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="51865-135">Note</span><span class="sxs-lookup"><span data-stu-id="51865-135">NOTES</span></span>

## <span data-ttu-id="51865-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51865-136">RELATED LINKS</span></span>
