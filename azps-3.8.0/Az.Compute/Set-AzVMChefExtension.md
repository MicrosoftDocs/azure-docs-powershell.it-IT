---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021387"
---
# <span data-ttu-id="9724a-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9724a-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="9724a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9724a-102">SYNOPSIS</span></span>
<span data-ttu-id="9724a-103">Aggiunge un'estensione di chef a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9724a-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="9724a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9724a-104">SYNTAX</span></span>

### <span data-ttu-id="9724a-105">Linux</span><span class="sxs-lookup"><span data-stu-id="9724a-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9724a-106">Windows</span><span class="sxs-lookup"><span data-stu-id="9724a-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9724a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9724a-107">DESCRIPTION</span></span>
<span data-ttu-id="9724a-108">Il cmdlet **set-AzVMChefExtension** aggiunge l'estensione chef alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9724a-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="9724a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9724a-109">EXAMPLES</span></span>

### <span data-ttu-id="9724a-110">Esempio 1: aggiungere un'estensione per lo chef a una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="9724a-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="9724a-111">Questo comando aggiunge un'estensione di chef a una macchina virtuale di Windows denominata WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="9724a-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="9724a-112">Al termine della macchina virtuale, lo chef avvia la macchina virtuale per eseguire Apache.</span><span class="sxs-lookup"><span data-stu-id="9724a-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="9724a-113">Esempio 2: aggiungere un'estensione per lo chef a una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="9724a-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="9724a-114">Questo comando aggiunge un'estensione di chef a una macchina virtuale di Linux denominata LinuxVM001.</span><span class="sxs-lookup"><span data-stu-id="9724a-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="9724a-115">Al termine della macchina virtuale, lo chef avvia la macchina virtuale per eseguire Apache.</span><span class="sxs-lookup"><span data-stu-id="9724a-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="9724a-116">Esempio 3: aggiungere un'estensione per lo chef a una macchina virtuale di Windows con le opzioni di bootstrap</span><span class="sxs-lookup"><span data-stu-id="9724a-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="9724a-117">Questo comando aggiunge l'estensione chef a una macchina virtuale di Windows denominata WindowsVM002.</span><span class="sxs-lookup"><span data-stu-id="9724a-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="9724a-118">Al termine della macchina virtuale, lo chef avvia la macchina virtuale per eseguire Apache.</span><span class="sxs-lookup"><span data-stu-id="9724a-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="9724a-119">Dopo l'avvio automatico, la macchina virtuale fa riferimento al BootstrapOptions specificato in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="9724a-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="9724a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9724a-120">PARAMETERS</span></span>

### <span data-ttu-id="9724a-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9724a-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9724a-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="9724a-122">-BootstrapOptions</span></span>
<span data-ttu-id="9724a-123">Specifica le impostazioni di configurazione nell'opzione client_rb.</span><span class="sxs-lookup"><span data-stu-id="9724a-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="9724a-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="9724a-124">-BootstrapVersion</span></span>
<span data-ttu-id="9724a-125">Specifica la versione della configurazione di bootstrap.</span><span class="sxs-lookup"><span data-stu-id="9724a-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="9724a-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="9724a-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="9724a-127">Specifica la frequenza (in minuti) in cui viene eseguito il servizio chef.</span><span class="sxs-lookup"><span data-stu-id="9724a-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="9724a-128">Se nel caso in cui non si vuole che il servizio chef venga installato in Azure VM, impostare il valore come 0 in questo campo.</span><span class="sxs-lookup"><span data-stu-id="9724a-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9724a-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="9724a-129">-ChefServerUrl</span></span>
<span data-ttu-id="9724a-130">Specifica il collegamento al server dello chef come URL.</span><span class="sxs-lookup"><span data-stu-id="9724a-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="9724a-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="9724a-131">-ClientRb</span></span>
<span data-ttu-id="9724a-132">Specifica il percorso completo dello chef client. RB.</span><span class="sxs-lookup"><span data-stu-id="9724a-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="9724a-133">-DAEMON</span><span class="sxs-lookup"><span data-stu-id="9724a-133">-Daemon</span></span>
<span data-ttu-id="9724a-134">Configura lo chef-servizio client per l'esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="9724a-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="9724a-135">La piattaforma node dovrebbe essere Windows.</span><span class="sxs-lookup"><span data-stu-id="9724a-135">The node platform should be Windows.</span></span>
<span data-ttu-id="9724a-136">Opzioni consentite: "nessuno", "servizio" e "attività".</span><span class="sxs-lookup"><span data-stu-id="9724a-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="9724a-137">Nessuno: al momento impedisce che il servizio chef-client venga configurato come servizio.</span><span class="sxs-lookup"><span data-stu-id="9724a-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="9724a-138">Service-configura lo chef-client in modo che venga eseguito automaticamente in background come servizio.</span><span class="sxs-lookup"><span data-stu-id="9724a-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="9724a-139">attività: configura lo chef-client in modo che venga eseguito automaticamente in background come attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="9724a-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9724a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9724a-140">-DefaultProfile</span></span>
<span data-ttu-id="9724a-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9724a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9724a-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="9724a-142">-JsonAttribute</span></span>
<span data-ttu-id="9724a-143">Una stringa JSON da aggiungere alla prima esecuzione di chef-client.</span><span class="sxs-lookup"><span data-stu-id="9724a-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="9724a-144">ad esempio-JsonAttribute ' {"foo": "bar"}'</span><span class="sxs-lookup"><span data-stu-id="9724a-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="9724a-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="9724a-145">-Linux</span></span>
<span data-ttu-id="9724a-146">Indica che questo cmdlet crea una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="9724a-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9724a-147">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9724a-147">-Location</span></span>
<span data-ttu-id="9724a-148">Specifica la posizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9724a-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9724a-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="9724a-149">-Name</span></span>
<span data-ttu-id="9724a-150">Specifica il nome dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="9724a-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9724a-151">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="9724a-151">-NoWait</span></span>
<span data-ttu-id="9724a-152">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9724a-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9724a-153">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="9724a-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9724a-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="9724a-154">-OrganizationName</span></span>
<span data-ttu-id="9724a-155">Specifica il nome dell'organizzazione dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="9724a-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="9724a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9724a-156">-ResourceGroupName</span></span>
<span data-ttu-id="9724a-157">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9724a-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="9724a-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="9724a-158">-RunList</span></span>
<span data-ttu-id="9724a-159">Specifica l'elenco di esecuzione dei nodi dello chef.</span><span class="sxs-lookup"><span data-stu-id="9724a-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="9724a-160">-Segreto</span><span class="sxs-lookup"><span data-stu-id="9724a-160">-Secret</span></span>
<span data-ttu-id="9724a-161">Chiave di crittografia utilizzata per crittografare e decrittografare i valori degli elementi del sacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="9724a-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="9724a-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="9724a-162">-SecretFile</span></span>
<span data-ttu-id="9724a-163">Percorso del file che contiene la chiave di crittografia utilizzata per crittografare e decrittografare i valori degli elementi del sacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="9724a-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="9724a-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9724a-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="9724a-165">Specifica la versione dell'estensione da usare per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9724a-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9724a-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="9724a-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="9724a-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="9724a-167">-ValidationPem</span></span>
<span data-ttu-id="9724a-168">Specifica il percorso del file di validator. pem dello chef</span><span class="sxs-lookup"><span data-stu-id="9724a-168">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="9724a-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="9724a-169">-VMName</span></span>
<span data-ttu-id="9724a-170">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9724a-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9724a-171">Questo cmdlet aggiunge l'estensione chef per la macchina virtuale specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9724a-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9724a-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="9724a-172">-Windows</span></span>
<span data-ttu-id="9724a-173">Indica che questo cmdlet crea una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="9724a-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9724a-174">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9724a-174">-Confirm</span></span>
<span data-ttu-id="9724a-175">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9724a-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9724a-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9724a-176">-WhatIf</span></span>
<span data-ttu-id="9724a-177">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9724a-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9724a-178">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9724a-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9724a-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9724a-179">CommonParameters</span></span>
<span data-ttu-id="9724a-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9724a-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9724a-181">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9724a-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9724a-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9724a-182">INPUTS</span></span>

### <span data-ttu-id="9724a-183">System. String</span><span class="sxs-lookup"><span data-stu-id="9724a-183">System.String</span></span>

### <span data-ttu-id="9724a-184">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9724a-184">System.Boolean</span></span>

## <span data-ttu-id="9724a-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9724a-185">OUTPUTS</span></span>

### <span data-ttu-id="9724a-186">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9724a-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9724a-187">Note</span><span class="sxs-lookup"><span data-stu-id="9724a-187">NOTES</span></span>

## <span data-ttu-id="9724a-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9724a-188">RELATED LINKS</span></span>

[<span data-ttu-id="9724a-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9724a-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="9724a-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9724a-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
