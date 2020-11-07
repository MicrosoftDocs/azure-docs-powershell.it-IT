---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: fed235e3c628ab245ae74299cf395e4501b141f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675191"
---
# <span data-ttu-id="5f509-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5f509-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="5f509-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f509-102">SYNOPSIS</span></span>
<span data-ttu-id="5f509-103">Aggiunge un'estensione di dominio Active Directory a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f509-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="5f509-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f509-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f509-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f509-105">DESCRIPTION</span></span>
<span data-ttu-id="5f509-106">Il cmdlet **set-AzVMADDomainExtension** aggiunge un'estensione della macchina virtuale Domain ad Azure Active Directory (ad) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f509-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="5f509-107">Questa estensione consente alla macchina virtuale di partecipare a un dominio.</span><span class="sxs-lookup"><span data-stu-id="5f509-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="5f509-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f509-108">EXAMPLES</span></span>

## <span data-ttu-id="5f509-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f509-109">PARAMETERS</span></span>

### <span data-ttu-id="5f509-110">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="5f509-110">-Credential</span></span>
<span data-ttu-id="5f509-111">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="5f509-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="5f509-112">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="5f509-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="5f509-113">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="5f509-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="5f509-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f509-114">-DefaultProfile</span></span>
<span data-ttu-id="5f509-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f509-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f509-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5f509-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="5f509-117">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="5f509-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="5f509-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="5f509-118">-DomainName</span></span>
<span data-ttu-id="5f509-119">Specifica il nome del dominio.</span><span class="sxs-lookup"><span data-stu-id="5f509-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="5f509-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5f509-120">-ForceRerun</span></span>
<span data-ttu-id="5f509-121">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="5f509-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5f509-122">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="5f509-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="5f509-123">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="5f509-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="5f509-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="5f509-124">-JoinOption</span></span>
<span data-ttu-id="5f509-125">Specifica l'opzione partecipa.</span><span class="sxs-lookup"><span data-stu-id="5f509-125">Specifies the join option.</span></span> <span data-ttu-id="5f509-126">Per le opzioni di join vedere [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="5f509-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="5f509-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5f509-127">-Location</span></span>
<span data-ttu-id="5f509-128">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f509-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5f509-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f509-129">-Name</span></span>
<span data-ttu-id="5f509-130">Specifica il nome dell'estensione del dominio da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="5f509-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="5f509-131">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="5f509-131">-NoWait</span></span>
<span data-ttu-id="5f509-132">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5f509-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5f509-133">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="5f509-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5f509-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="5f509-134">-OUPath</span></span>
<span data-ttu-id="5f509-135">Specifica un'unità organizzativa per l'account di dominio.</span><span class="sxs-lookup"><span data-stu-id="5f509-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="5f509-136">Immettere il nome distinto completo dell'unità organizzativa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="5f509-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="5f509-137">Il valore predefinito è l'unità organizzativa predefinita per gli oggetti computer nel dominio.</span><span class="sxs-lookup"><span data-stu-id="5f509-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="5f509-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f509-138">-ResourceGroupName</span></span>
<span data-ttu-id="5f509-139">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f509-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5f509-140">-Riavviare</span><span class="sxs-lookup"><span data-stu-id="5f509-140">-Restart</span></span>
<span data-ttu-id="5f509-141">Indica che questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f509-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="5f509-142">È spesso necessario riavviare un riavvio per rendere effettiva la modifica.</span><span class="sxs-lookup"><span data-stu-id="5f509-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="5f509-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5f509-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="5f509-144">Specifica la versione dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="5f509-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="5f509-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="5f509-145">-VMName</span></span>
<span data-ttu-id="5f509-146">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f509-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="5f509-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f509-147">-Confirm</span></span>
<span data-ttu-id="5f509-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f509-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f509-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f509-149">-WhatIf</span></span>
<span data-ttu-id="5f509-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f509-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f509-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f509-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f509-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f509-152">CommonParameters</span></span>
<span data-ttu-id="5f509-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f509-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f509-154">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f509-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f509-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f509-155">INPUTS</span></span>

### <span data-ttu-id="5f509-156">System. String</span><span class="sxs-lookup"><span data-stu-id="5f509-156">System.String</span></span>

### <span data-ttu-id="5f509-157">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5f509-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5f509-158">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="5f509-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="5f509-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5f509-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5f509-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f509-160">OUTPUTS</span></span>

### <span data-ttu-id="5f509-161">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5f509-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5f509-162">Note</span><span class="sxs-lookup"><span data-stu-id="5f509-162">NOTES</span></span>

## <span data-ttu-id="5f509-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f509-163">RELATED LINKS</span></span>

[<span data-ttu-id="5f509-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5f509-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)