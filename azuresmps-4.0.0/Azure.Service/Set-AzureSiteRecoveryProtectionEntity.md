---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029885"
---
# <span data-ttu-id="a8153-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a8153-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="a8153-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8153-102">SYNOPSIS</span></span>
<span data-ttu-id="a8153-103">Imposta lo stato per un'entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="a8153-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="a8153-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8153-104">SYNTAX</span></span>

### <span data-ttu-id="a8153-105">ByPEObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8153-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8153-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="a8153-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8153-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8153-107">DESCRIPTION</span></span>
<span data-ttu-id="a8153-108">Il cmdlet **set-AzureSiteRecoveryProtectionEntity** Abilita o Disabilita la protezione in un'entità di protezione del ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8153-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="a8153-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8153-109">EXAMPLES</span></span>

### <span data-ttu-id="a8153-110">Esempio 1: abilitare la protezione per gli oggetti in un contenitore</span><span class="sxs-lookup"><span data-stu-id="a8153-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="a8153-111">Il primo comando ottiene i contenitori per il Vault del sito di Azure corrente usando il cmdlet **Get-AzureSiteRecoveryProtectionContainer** e lo archivia nella variabile $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="a8153-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="a8153-112">Il secondo comando ottiene le macchine virtuali protette che appartengono al contenitore archiviato in $ProtectionContainer usando il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="a8153-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="a8153-113">Il comando Archivia i risultati nella variabile $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="a8153-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="a8153-114">Il comando finale consente la protezione per le entità archiviate in $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="a8153-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="a8153-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8153-115">PARAMETERS</span></span>

### <span data-ttu-id="a8153-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a8153-116">-Force</span></span>
<span data-ttu-id="a8153-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a8153-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8153-118">-ID</span><span class="sxs-lookup"><span data-stu-id="a8153-118">-Id</span></span>
<span data-ttu-id="a8153-119">Specifica l'ID di una macchina virtuale protetta per cui abilitare o disabilitare la protezione.</span><span class="sxs-lookup"><span data-stu-id="a8153-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8153-120">-OS</span><span class="sxs-lookup"><span data-stu-id="a8153-120">-OS</span></span>
<span data-ttu-id="a8153-121">Specifica il tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a8153-121">Specifies the operating system type.</span></span>
<span data-ttu-id="a8153-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8153-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8153-123">Windows</span><span class="sxs-lookup"><span data-stu-id="a8153-123">Windows</span></span>
- <span data-ttu-id="a8153-124">Linux</span><span class="sxs-lookup"><span data-stu-id="a8153-124">Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8153-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="a8153-125">-OSDiskName</span></span>
<span data-ttu-id="a8153-126">Specifica il nome del disco che contiene il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a8153-126">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8153-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="a8153-127">-Profile</span></span>
<span data-ttu-id="a8153-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8153-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8153-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a8153-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8153-130">-Protezione</span><span class="sxs-lookup"><span data-stu-id="a8153-130">-Protection</span></span>
<span data-ttu-id="a8153-131">Specifica se la protezione deve essere abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a8153-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="a8153-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8153-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8153-133">Abilita</span><span class="sxs-lookup"><span data-stu-id="a8153-133">Enable</span></span>
- <span data-ttu-id="a8153-134">Disabilitare</span><span class="sxs-lookup"><span data-stu-id="a8153-134">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8153-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="a8153-135">-ProtectionContainerId</span></span>
<span data-ttu-id="a8153-136">Specifica l'ID di un contenitore protetto.</span><span class="sxs-lookup"><span data-stu-id="a8153-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="a8153-137">Questo cmdlet Abilita o Disabilita la protezione per una macchina virtuale che appartiene al contenitore specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a8153-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8153-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a8153-138">-ProtectionEntity</span></span>
<span data-ttu-id="a8153-139">Specifica l'oggetto entità di protezione.</span><span class="sxs-lookup"><span data-stu-id="a8153-139">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8153-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="a8153-140">-ProtectionProfile</span></span>
<span data-ttu-id="a8153-141">Specifica un profilo di protezione per abilitare la protezione.</span><span class="sxs-lookup"><span data-stu-id="a8153-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="a8153-142">Specifica un oggetto **ASRProtectionProfile** che rappresenta uno dei profili di protezione disponibili nel contenitore di protezione associato.</span><span class="sxs-lookup"><span data-stu-id="a8153-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8153-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a8153-143">-WaitForCompletion</span></span>
<span data-ttu-id="a8153-144">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8153-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="a8153-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8153-145">-Confirm</span></span>
<span data-ttu-id="a8153-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8153-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8153-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8153-147">-WhatIf</span></span>
<span data-ttu-id="a8153-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8153-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8153-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8153-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8153-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8153-150">CommonParameters</span></span>
<span data-ttu-id="a8153-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8153-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8153-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8153-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8153-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8153-153">INPUTS</span></span>

## <span data-ttu-id="a8153-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8153-154">OUTPUTS</span></span>

## <span data-ttu-id="a8153-155">Note</span><span class="sxs-lookup"><span data-stu-id="a8153-155">NOTES</span></span>

## <span data-ttu-id="a8153-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8153-156">RELATED LINKS</span></span>

[<span data-ttu-id="a8153-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a8153-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="a8153-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a8153-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="a8153-159">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a8153-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


