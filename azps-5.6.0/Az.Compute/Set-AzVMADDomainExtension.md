---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 03f898246b2f0d784725488f753697ed893b09df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015405"
---
# <span data-ttu-id="bfe90-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="bfe90-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="bfe90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfe90-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe90-103">Aggiunge un'estensione di dominio Active Directory a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bfe90-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="bfe90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfe90-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfe90-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfe90-105">DESCRIPTION</span></span>
<span data-ttu-id="bfe90-106">Il cmdlet **Set-AzVMADDomainExtension** aggiunge un'estensione di macchina virtuale del dominio di Azure Active Directory (AD) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bfe90-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="bfe90-107">Questa estensione consente alla macchina virtuale di aggiungere un dominio.</span><span class="sxs-lookup"><span data-stu-id="bfe90-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="bfe90-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfe90-108">EXAMPLES</span></span>

## <span data-ttu-id="bfe90-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfe90-109">PARAMETERS</span></span>

### <span data-ttu-id="bfe90-110">-Credential</span><span class="sxs-lookup"><span data-stu-id="bfe90-110">-Credential</span></span>
<span data-ttu-id="bfe90-111">Specifica il nome utente e la password della macchina virtuale come **oggetto PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="bfe90-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="bfe90-112">Per ottenere le credenziali, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="bfe90-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="bfe90-113">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="bfe90-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe90-114">-DefaultProfile</span></span>
<span data-ttu-id="bfe90-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfe90-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfe90-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bfe90-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bfe90-117">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="bfe90-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="bfe90-118">-DomainName</span></span>
<span data-ttu-id="bfe90-119">Specifica il nome del dominio.</span><span class="sxs-lookup"><span data-stu-id="bfe90-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="bfe90-120">-ForceRerun</span></span>
<span data-ttu-id="bfe90-121">Indica che questo cmdlet forza una nuova esecuzione della stessa configurazione dell'estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="bfe90-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="bfe90-122">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="bfe90-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="bfe90-123">Se forceUpdateTag non viene modificato, gli aggiornamenti alle impostazioni pubbliche o protette vengono comunque applicati dal gestore.</span><span class="sxs-lookup"><span data-stu-id="bfe90-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="bfe90-124">-JoinOption</span></span>
<span data-ttu-id="bfe90-125">Specifica l'opzione di join.</span><span class="sxs-lookup"><span data-stu-id="bfe90-125">Specifies the join option.</span></span> <span data-ttu-id="bfe90-126">Per le opzioni di join, [vedere fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="bfe90-126">For join options see [fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-127">-Location</span><span class="sxs-lookup"><span data-stu-id="bfe90-127">-Location</span></span>
<span data-ttu-id="bfe90-128">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bfe90-128">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-129">-Name</span><span class="sxs-lookup"><span data-stu-id="bfe90-129">-Name</span></span>
<span data-ttu-id="bfe90-130">Specifica il nome dell'estensione di dominio da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfe90-130">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bfe90-131">-NoWait</span></span>
<span data-ttu-id="bfe90-132">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bfe90-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bfe90-133">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="bfe90-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bfe90-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="bfe90-134">-OUPath</span></span>
<span data-ttu-id="bfe90-135">Specifica un'unità organizzativa (OU) per l'account di dominio.</span><span class="sxs-lookup"><span data-stu-id="bfe90-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="bfe90-136">Immettere il nome distinto completo dell'unità organizzativa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="bfe90-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="bfe90-137">Il valore predefinito è l'unità organizzativa predefinita per gli oggetti computer nel dominio.</span><span class="sxs-lookup"><span data-stu-id="bfe90-137">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfe90-138">-ResourceGroupName</span></span>
<span data-ttu-id="bfe90-139">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfe90-139">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-140">-Riavvia</span><span class="sxs-lookup"><span data-stu-id="bfe90-140">-Restart</span></span>
<span data-ttu-id="bfe90-141">Indica che questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bfe90-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="bfe90-142">Per rendere effettiva la modifica è spesso necessario un riavvio.</span><span class="sxs-lookup"><span data-stu-id="bfe90-142">A restart is often required to make the change effective.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bfe90-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="bfe90-144">Specifica la versione dell'estensione di dominio.</span><span class="sxs-lookup"><span data-stu-id="bfe90-144">Specifies the version of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="bfe90-145">-VMName</span></span>
<span data-ttu-id="bfe90-146">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bfe90-146">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfe90-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfe90-147">-Confirm</span></span>
<span data-ttu-id="bfe90-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfe90-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfe90-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfe90-149">-WhatIf</span></span>
<span data-ttu-id="bfe90-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfe90-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfe90-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfe90-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfe90-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe90-152">CommonParameters</span></span>
<span data-ttu-id="bfe90-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfe90-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe90-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfe90-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe90-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfe90-155">INPUTS</span></span>

### <span data-ttu-id="bfe90-156">System.String</span><span class="sxs-lookup"><span data-stu-id="bfe90-156">System.String</span></span>

### <span data-ttu-id="bfe90-157">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bfe90-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bfe90-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="bfe90-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="bfe90-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bfe90-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bfe90-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfe90-160">OUTPUTS</span></span>

### <span data-ttu-id="bfe90-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bfe90-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bfe90-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfe90-162">NOTES</span></span>

## <span data-ttu-id="bfe90-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfe90-163">RELATED LINKS</span></span>

[<span data-ttu-id="bfe90-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="bfe90-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
