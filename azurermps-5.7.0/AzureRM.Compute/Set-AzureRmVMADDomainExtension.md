---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508315"
---
# <span data-ttu-id="82cd2-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="82cd2-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="82cd2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="82cd2-103">Aggiunge un'estensione di dominio Active Directory a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="82cd2-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82cd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82cd2-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82cd2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="82cd2-106">Il cmdlet **set-AzureRmVMADDomainExtension** aggiunge un'estensione della macchina virtuale Domain ad Azure Active Directory (ad) a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="82cd2-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="82cd2-107">Questa estensione consente alla macchina virtuale di partecipare a un dominio.</span><span class="sxs-lookup"><span data-stu-id="82cd2-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="82cd2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82cd2-108">EXAMPLES</span></span>

## <span data-ttu-id="82cd2-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82cd2-109">PARAMETERS</span></span>

### <span data-ttu-id="82cd2-110">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="82cd2-110">-Credential</span></span>
<span data-ttu-id="82cd2-111">Specifica il nome utente e la password per la macchina virtuale come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="82cd2-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="82cd2-112">Per ottenere una credenziale, usare il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="82cd2-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="82cd2-113">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="82cd2-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="82cd2-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="82cd2-115">Indica che questo cmdlet disabilita l'aggiornamento automatico della versione secondaria dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="82cd2-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-116">-DomainName</span><span class="sxs-lookup"><span data-stu-id="82cd2-116">-DomainName</span></span>
<span data-ttu-id="82cd2-117">Specifica il nome del dominio.</span><span class="sxs-lookup"><span data-stu-id="82cd2-117">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="82cd2-118">-ForceRerun</span></span>
<span data-ttu-id="82cd2-119">Indica che questo cmdlet impone la ripetizione della stessa configurazione di estensione nella macchina virtuale senza disinstallare e reinstallare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="82cd2-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="82cd2-120">Il valore può essere qualsiasi stringa diversa dal valore corrente.</span><span class="sxs-lookup"><span data-stu-id="82cd2-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="82cd2-121">Se forceUpdateTag non viene modificato, le modifiche apportate alle impostazioni pubbliche o protette verranno ancora applicate dal gestore.</span><span class="sxs-lookup"><span data-stu-id="82cd2-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="82cd2-122">-JoinOption</span></span>
<span data-ttu-id="82cd2-123">Specifica l'opzione partecipa.</span><span class="sxs-lookup"><span data-stu-id="82cd2-123">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="82cd2-124">-Location</span></span>
<span data-ttu-id="82cd2-125">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="82cd2-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="82cd2-126">-Name</span></span>
<span data-ttu-id="82cd2-127">Specifica il nome dell'estensione del dominio da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="82cd2-127">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="82cd2-128">-OUPath</span></span>
<span data-ttu-id="82cd2-129">Specifica un'unità organizzativa per l'account di dominio.</span><span class="sxs-lookup"><span data-stu-id="82cd2-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="82cd2-130">Immettere il nome distinto completo dell'unità organizzativa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="82cd2-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="82cd2-131">Il valore predefinito è l'unità organizzativa predefinita per gli oggetti computer nel dominio.</span><span class="sxs-lookup"><span data-stu-id="82cd2-131">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82cd2-132">-ResourceGroupName</span></span>
<span data-ttu-id="82cd2-133">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="82cd2-133">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-134">-Riavviare</span><span class="sxs-lookup"><span data-stu-id="82cd2-134">-Restart</span></span>
<span data-ttu-id="82cd2-135">Indica che questo cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="82cd2-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="82cd2-136">È spesso necessario riavviare un riavvio per rendere effettiva la modifica.</span><span class="sxs-lookup"><span data-stu-id="82cd2-136">A restart is often required to make the change effective.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="82cd2-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="82cd2-138">Specifica la versione dell'estensione del dominio.</span><span class="sxs-lookup"><span data-stu-id="82cd2-138">Specifies the version of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="82cd2-139">-VMName</span></span>
<span data-ttu-id="82cd2-140">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="82cd2-140">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82cd2-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82cd2-141">-Confirm</span></span>
<span data-ttu-id="82cd2-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82cd2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82cd2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82cd2-143">-WhatIf</span></span>
<span data-ttu-id="82cd2-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82cd2-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="82cd2-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82cd2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82cd2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82cd2-146">CommonParameters</span></span>
<span data-ttu-id="82cd2-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82cd2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82cd2-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82cd2-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82cd2-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82cd2-149">INPUTS</span></span>

### <span data-ttu-id="82cd2-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82cd2-150">None</span></span>
<span data-ttu-id="82cd2-151">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="82cd2-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82cd2-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82cd2-152">OUTPUTS</span></span>

## <span data-ttu-id="82cd2-153">Note</span><span class="sxs-lookup"><span data-stu-id="82cd2-153">NOTES</span></span>

## <span data-ttu-id="82cd2-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82cd2-154">RELATED LINKS</span></span>

[<span data-ttu-id="82cd2-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="82cd2-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
