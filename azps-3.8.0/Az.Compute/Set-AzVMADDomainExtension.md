---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 1ea90503c1d022aa5a1925fa489e2ee63f4560ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018875"
---
# <span data-ttu-id="bc6fd-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="bc6fd-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="bc6fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc6fd-102">SYNOPSIS</span></span>
<span data-ttu-id="bc6fd-103">Aggiunge un'estensione di dominio Active Directory a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="bc6fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc6fd-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc6fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc6fd-105">DESCRIPTION</span></span>
<span data-ttu-id="bc6fd-106">Il cmdlet **set-AzVMADDomainExtension** aggiunge un'estensione della macchina virtuale Domain ad Azure Active Directory (ad) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="bc6fd-107">Questa estensione consente alla macchina virtuale di partecipare a un dominio.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="bc6fd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc6fd-108">EXAMPLES</span></span>

## <span data-ttu-id="bc6fd-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc6fd-109">PARAMETERS</span></span>

### <span data-ttu-id="bc6fd-110">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="bc6fd-110">-Credential</span></span>
<span data-ttu-id="bc6fd-111">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="bc6fd-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="bc6fd-112">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="bc6fd-113">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="bc6fd-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="bc6fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc6fd-114">-DefaultProfile</span></span>
<span data-ttu-id="bc6fd-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc6fd-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bc6fd-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bc6fd-117">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="bc6fd-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="bc6fd-118">-DomainName</span></span>
<span data-ttu-id="bc6fd-119">Specifica il nome del dominio.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="bc6fd-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="bc6fd-120">-ForceRerun</span></span>
<span data-ttu-id="bc6fd-121">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="bc6fd-122">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="bc6fd-123">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="bc6fd-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="bc6fd-124">-JoinOption</span></span>
<span data-ttu-id="bc6fd-125">Specifica l'opzione partecipa.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-125">Specifies the join option.</span></span> <span data-ttu-id="bc6fd-126">Per le opzioni di join vedere [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="bc6fd-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="bc6fd-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bc6fd-127">-Location</span></span>
<span data-ttu-id="bc6fd-128">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="bc6fd-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc6fd-129">-Name</span></span>
<span data-ttu-id="bc6fd-130">Specifica il nome dell'estensione del dominio da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="bc6fd-131">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="bc6fd-131">-NoWait</span></span>
<span data-ttu-id="bc6fd-132">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bc6fd-133">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bc6fd-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="bc6fd-134">-OUPath</span></span>
<span data-ttu-id="bc6fd-135">Specifica un'unità organizzativa per l'account di dominio.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="bc6fd-136">Immettere il nome distinto completo dell'unità organizzativa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="bc6fd-137">Il valore predefinito è l'unità organizzativa predefinita per gli oggetti computer nel dominio.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="bc6fd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc6fd-138">-ResourceGroupName</span></span>
<span data-ttu-id="bc6fd-139">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bc6fd-140">-Riavviare</span><span class="sxs-lookup"><span data-stu-id="bc6fd-140">-Restart</span></span>
<span data-ttu-id="bc6fd-141">Indica che questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="bc6fd-142">È spesso necessario riavviare un riavvio per rendere effettiva la modifica.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="bc6fd-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bc6fd-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="bc6fd-144">Specifica la versione dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="bc6fd-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="bc6fd-145">-VMName</span></span>
<span data-ttu-id="bc6fd-146">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="bc6fd-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc6fd-147">-Confirm</span></span>
<span data-ttu-id="bc6fd-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc6fd-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc6fd-149">-WhatIf</span></span>
<span data-ttu-id="bc6fd-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc6fd-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc6fd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc6fd-152">CommonParameters</span></span>
<span data-ttu-id="bc6fd-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc6fd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc6fd-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc6fd-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc6fd-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc6fd-155">INPUTS</span></span>

### <span data-ttu-id="bc6fd-156">System. String</span><span class="sxs-lookup"><span data-stu-id="bc6fd-156">System.String</span></span>

### <span data-ttu-id="bc6fd-157">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc6fd-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bc6fd-158">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="bc6fd-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="bc6fd-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bc6fd-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bc6fd-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc6fd-160">OUTPUTS</span></span>

### <span data-ttu-id="bc6fd-161">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bc6fd-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bc6fd-162">Note</span><span class="sxs-lookup"><span data-stu-id="bc6fd-162">NOTES</span></span>

## <span data-ttu-id="bc6fd-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc6fd-163">RELATED LINKS</span></span>

[<span data-ttu-id="bc6fd-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="bc6fd-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
