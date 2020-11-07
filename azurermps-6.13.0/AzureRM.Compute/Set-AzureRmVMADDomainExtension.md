---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e0d36e8ddc239d1d075b79e0c91df645d671c6a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521392"
---
# <span data-ttu-id="fe2ae-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fe2ae-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="fe2ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe2ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2ae-103">Aggiunge un'estensione di dominio Active Directory a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe2ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe2ae-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe2ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe2ae-105">DESCRIPTION</span></span>
<span data-ttu-id="fe2ae-106">Il cmdlet **set-AzureRmVMADDomainExtension** aggiunge un'estensione della macchina virtuale Domain ad Azure Active Directory (ad) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="fe2ae-107">Questa estensione consente alla macchina virtuale di partecipare a un dominio.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="fe2ae-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe2ae-108">EXAMPLES</span></span>

## <span data-ttu-id="fe2ae-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe2ae-109">PARAMETERS</span></span>

### <span data-ttu-id="fe2ae-110">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="fe2ae-110">-Credential</span></span>
<span data-ttu-id="fe2ae-111">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="fe2ae-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="fe2ae-112">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="fe2ae-113">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="fe2ae-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="fe2ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2ae-114">-DefaultProfile</span></span>
<span data-ttu-id="fe2ae-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe2ae-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fe2ae-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fe2ae-117">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="fe2ae-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="fe2ae-118">-DomainName</span></span>
<span data-ttu-id="fe2ae-119">Specifica il nome del dominio.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="fe2ae-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="fe2ae-120">-ForceRerun</span></span>
<span data-ttu-id="fe2ae-121">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="fe2ae-122">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="fe2ae-123">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="fe2ae-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="fe2ae-124">-JoinOption</span></span>
<span data-ttu-id="fe2ae-125">Specifica l'opzione partecipa.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-125">Specifies the join option.</span></span> <span data-ttu-id="fe2ae-126">Per le opzioni di join vedere [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="fe2ae-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="fe2ae-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="fe2ae-127">-Location</span></span>
<span data-ttu-id="fe2ae-128">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="fe2ae-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe2ae-129">-Name</span></span>
<span data-ttu-id="fe2ae-130">Specifica il nome dell'estensione del dominio da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="fe2ae-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="fe2ae-131">-OUPath</span></span>
<span data-ttu-id="fe2ae-132">Specifica un'unità organizzativa per l'account di dominio.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="fe2ae-133">Immettere il nome distinto completo dell'unità organizzativa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="fe2ae-134">Il valore predefinito è l'unità organizzativa predefinita per gli oggetti computer nel dominio.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-134">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="fe2ae-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe2ae-135">-ResourceGroupName</span></span>
<span data-ttu-id="fe2ae-136">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fe2ae-137">-Riavviare</span><span class="sxs-lookup"><span data-stu-id="fe2ae-137">-Restart</span></span>
<span data-ttu-id="fe2ae-138">Indica che questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="fe2ae-139">È spesso necessario riavviare un riavvio per rendere effettiva la modifica.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-139">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="fe2ae-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fe2ae-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="fe2ae-141">Specifica la versione dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-141">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="fe2ae-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="fe2ae-142">-VMName</span></span>
<span data-ttu-id="fe2ae-143">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-143">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="fe2ae-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe2ae-144">-Confirm</span></span>
<span data-ttu-id="fe2ae-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe2ae-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe2ae-146">-WhatIf</span></span>
<span data-ttu-id="fe2ae-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe2ae-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe2ae-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2ae-149">CommonParameters</span></span>
<span data-ttu-id="fe2ae-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2ae-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2ae-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2ae-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2ae-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe2ae-152">INPUTS</span></span>

### <span data-ttu-id="fe2ae-153">System. String</span><span class="sxs-lookup"><span data-stu-id="fe2ae-153">System.String</span></span>

### <span data-ttu-id="fe2ae-154">System. Nullable ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fe2ae-154">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fe2ae-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="fe2ae-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="fe2ae-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fe2ae-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe2ae-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe2ae-157">OUTPUTS</span></span>

### <span data-ttu-id="fe2ae-158">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fe2ae-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fe2ae-159">Note</span><span class="sxs-lookup"><span data-stu-id="fe2ae-159">NOTES</span></span>

## <span data-ttu-id="fe2ae-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe2ae-160">RELATED LINKS</span></span>

[<span data-ttu-id="fe2ae-161">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fe2ae-161">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)