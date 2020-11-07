---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685972"
---
# <span data-ttu-id="56e6d-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="56e6d-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="56e6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="56e6d-103">Imposta lo stato per un'entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="56e6d-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56e6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56e6d-104">SYNTAX</span></span>

### <span data-ttu-id="56e6d-105">Disabler (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56e6d-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56e6d-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="56e6d-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e6d-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="56e6d-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56e6d-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="56e6d-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56e6d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56e6d-109">DESCRIPTION</span></span>
<span data-ttu-id="56e6d-110">Il cmdlet **set-AzureRmSiteRecoveryProtectionEntity** Abilita o Disabilita la protezione in un'entità di protezione del ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e6d-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="56e6d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56e6d-111">EXAMPLES</span></span>

## <span data-ttu-id="56e6d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56e6d-112">PARAMETERS</span></span>

### <span data-ttu-id="56e6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e6d-113">-DefaultProfile</span></span>
<span data-ttu-id="56e6d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56e6d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e6d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56e6d-115">-Force</span></span>
<span data-ttu-id="56e6d-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="56e6d-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-117">-OS</span><span class="sxs-lookup"><span data-stu-id="56e6d-117">-OS</span></span>
<span data-ttu-id="56e6d-118">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="56e6d-118">Specifies the operating system type.</span></span>
<span data-ttu-id="56e6d-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="56e6d-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56e6d-120">Windows</span><span class="sxs-lookup"><span data-stu-id="56e6d-120">Windows</span></span>
- <span data-ttu-id="56e6d-121">Linux</span><span class="sxs-lookup"><span data-stu-id="56e6d-121">Linux</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-122">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="56e6d-122">-OSDiskName</span></span>
<span data-ttu-id="56e6d-123">Specifica il nome del disco che contiene il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="56e6d-123">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-124">-Policy</span><span class="sxs-lookup"><span data-stu-id="56e6d-124">-Policy</span></span>
<span data-ttu-id="56e6d-125">Specifica l'oggetto Criteri di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="56e6d-125">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-126">-Protezione</span><span class="sxs-lookup"><span data-stu-id="56e6d-126">-Protection</span></span>
<span data-ttu-id="56e6d-127">Specifica se la protezione deve essere abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="56e6d-127">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="56e6d-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="56e6d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56e6d-129">Abilita</span><span class="sxs-lookup"><span data-stu-id="56e6d-129">Enable</span></span>
- <span data-ttu-id="56e6d-130">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="56e6d-130">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-131">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="56e6d-131">-ProtectionEntity</span></span>
<span data-ttu-id="56e6d-132">Specifica l'oggetto entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="56e6d-132">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-133">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="56e6d-133">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="56e6d-134">Specifica l'ID dell'account di archiviazione di Azure di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56e6d-134">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-135">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="56e6d-135">-WaitForCompletion</span></span>
<span data-ttu-id="56e6d-136">Indica che il comando attende il completamento prima della restituzione.</span><span class="sxs-lookup"><span data-stu-id="56e6d-136">Indicates that the command waits for completion before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56e6d-137">-Confirm</span></span>
<span data-ttu-id="56e6d-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e6d-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e6d-139">-WhatIf</span></span>
<span data-ttu-id="56e6d-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56e6d-140">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="56e6d-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56e6d-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56e6d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e6d-142">CommonParameters</span></span>
<span data-ttu-id="56e6d-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e6d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e6d-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56e6d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e6d-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56e6d-145">INPUTS</span></span>

### <span data-ttu-id="56e6d-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="56e6d-146">ASRProtectionEntity</span></span>
<span data-ttu-id="56e6d-147">Il parametro ' ProtectionEntity ' accetta il valore di tipo ' ASRProtectionEntity ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="56e6d-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="56e6d-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56e6d-148">OUTPUTS</span></span>

### <span data-ttu-id="56e6d-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="56e6d-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56e6d-150">Note</span><span class="sxs-lookup"><span data-stu-id="56e6d-150">NOTES</span></span>

## <span data-ttu-id="56e6d-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56e6d-151">RELATED LINKS</span></span>

[<span data-ttu-id="56e6d-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="56e6d-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
