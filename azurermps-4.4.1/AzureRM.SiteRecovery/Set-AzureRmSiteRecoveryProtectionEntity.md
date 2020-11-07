---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 245eb56ea973c1330b7f8b9d32a3f0b9584bd0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686771"
---
# <span data-ttu-id="8bc37-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8bc37-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="8bc37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bc37-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc37-103">Imposta lo stato per un'entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="8bc37-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bc37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bc37-104">SYNTAX</span></span>

### <span data-ttu-id="8bc37-105">Disabler (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8bc37-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bc37-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8bc37-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc37-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="8bc37-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc37-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="8bc37-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bc37-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bc37-109">DESCRIPTION</span></span>
<span data-ttu-id="8bc37-110">Il cmdlet **set-AzureRmSiteRecoveryProtectionEntity** Abilita o Disabilita la protezione in un'entità di protezione del ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc37-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="8bc37-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bc37-111">EXAMPLES</span></span>

## <span data-ttu-id="8bc37-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bc37-112">PARAMETERS</span></span>

### <span data-ttu-id="8bc37-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8bc37-113">-Force</span></span>
<span data-ttu-id="8bc37-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8bc37-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-115">-OS</span><span class="sxs-lookup"><span data-stu-id="8bc37-115">-OS</span></span>
<span data-ttu-id="8bc37-116">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8bc37-116">Specifies the operating system type.</span></span>
<span data-ttu-id="8bc37-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8bc37-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8bc37-118">Windows</span><span class="sxs-lookup"><span data-stu-id="8bc37-118">Windows</span></span>
- <span data-ttu-id="8bc37-119">Linux</span><span class="sxs-lookup"><span data-stu-id="8bc37-119">Linux</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-120">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="8bc37-120">-OSDiskName</span></span>
<span data-ttu-id="8bc37-121">Specifica il nome del disco che contiene il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8bc37-121">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-122">-Policy</span><span class="sxs-lookup"><span data-stu-id="8bc37-122">-Policy</span></span>
<span data-ttu-id="8bc37-123">Specifica l'oggetto Criteri di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="8bc37-123">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-124">-Protezione</span><span class="sxs-lookup"><span data-stu-id="8bc37-124">-Protection</span></span>
<span data-ttu-id="8bc37-125">Specifica se la protezione deve essere abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="8bc37-125">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="8bc37-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8bc37-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8bc37-127">Abilita</span><span class="sxs-lookup"><span data-stu-id="8bc37-127">Enable</span></span>
- <span data-ttu-id="8bc37-128">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="8bc37-128">Disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8bc37-129">-ProtectionEntity</span></span>
<span data-ttu-id="8bc37-130">Specifica l'oggetto entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="8bc37-130">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-131">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8bc37-131">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8bc37-132">Specifica l'ID dell'account di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8bc37-132">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-133">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="8bc37-133">-WaitForCompletion</span></span>
<span data-ttu-id="8bc37-134">Indica che il comando attende il completamento prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="8bc37-134">Indicates that the command waits for completion before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8bc37-135">-Confirm</span></span>
<span data-ttu-id="8bc37-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc37-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc37-137">-WhatIf</span></span>
<span data-ttu-id="8bc37-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bc37-138">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8bc37-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bc37-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc37-140">-DefaultProfile</span></span>
<span data-ttu-id="8bc37-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc37-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bc37-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc37-142">CommonParameters</span></span>
<span data-ttu-id="8bc37-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc37-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc37-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc37-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc37-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bc37-145">INPUTS</span></span>

### <span data-ttu-id="8bc37-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8bc37-146">ASRProtectionEntity</span></span>
<span data-ttu-id="8bc37-147">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8bc37-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="8bc37-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bc37-148">OUTPUTS</span></span>

### <span data-ttu-id="8bc37-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8bc37-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8bc37-150">Note</span><span class="sxs-lookup"><span data-stu-id="8bc37-150">NOTES</span></span>

## <span data-ttu-id="8bc37-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bc37-151">RELATED LINKS</span></span>

[<span data-ttu-id="8bc37-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8bc37-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
