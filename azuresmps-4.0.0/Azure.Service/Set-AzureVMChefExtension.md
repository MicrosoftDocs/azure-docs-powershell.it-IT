---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029507"
---
# <span data-ttu-id="62943-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="62943-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="62943-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62943-102">SYNOPSIS</span></span>
<span data-ttu-id="62943-103">Aggiunge l'estensione dello chef alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="62943-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="62943-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62943-104">SYNTAX</span></span>

### <span data-ttu-id="62943-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62943-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="62943-106">Linux</span><span class="sxs-lookup"><span data-stu-id="62943-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="62943-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62943-107">DESCRIPTION</span></span>
<span data-ttu-id="62943-108">Il cmdlet **set-AzureVMChefExtension** aggiunge l'estensione chef alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="62943-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="62943-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62943-109">EXAMPLES</span></span>

### <span data-ttu-id="62943-110">Esempio 1: aggiungere un'estensione per lo chef a una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="62943-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="62943-111">Questo comando aggiunge un'estensione di chef a una macchina virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="62943-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="62943-112">Quando la macchina virtuale viene attivata, viene avviata con lo chef ed esegue Apache.</span><span class="sxs-lookup"><span data-stu-id="62943-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="62943-113">Esempio 2: aggiungere un'estensione per lo chef a una macchina virtuale di Windows con l'avvio automatico</span><span class="sxs-lookup"><span data-stu-id="62943-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="62943-114">Questo comando aggiunge l'estensione dello chef a una macchina virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="62943-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="62943-115">Quando la macchina virtuale viene lanciata, viene avviata con lo chef ed esegue Apache.</span><span class="sxs-lookup"><span data-stu-id="62943-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="62943-116">Dopo l'avvio automatico, la macchina virtuale fa riferimento al *BootstrapOptions* specificato in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="62943-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="62943-117">Esempio 3: aggiungere un'estensione per lo chef a una macchina virtuale di Windows e installare Apache e GIT</span><span class="sxs-lookup"><span data-stu-id="62943-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="62943-118">Questo comando aggiunge l'estensione dello chef a una macchina virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="62943-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="62943-119">Quando la macchina virtuale viene lanciata, viene avviata con lo chef e sono installati Apache e GIT.</span><span class="sxs-lookup"><span data-stu-id="62943-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="62943-120">Se non si specifica il client. RB, è necessario specificare l'URL del server dello chef e il nome del client di convalida.</span><span class="sxs-lookup"><span data-stu-id="62943-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="62943-121">Esempio 4: aggiungere un'estensione per lo chef a una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="62943-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="62943-122">Questo comando aggiunge l'estensione dello chef a una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="62943-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="62943-123">Quando la macchina virtuale viene avviata, viene avviato con lo chef.</span><span class="sxs-lookup"><span data-stu-id="62943-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="62943-124">Se non si specifica il client. RB, è necessario specificare l'URL e l'organizzazione del server dello chef.</span><span class="sxs-lookup"><span data-stu-id="62943-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="62943-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62943-125">PARAMETERS</span></span>

### <span data-ttu-id="62943-126">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="62943-126">-BootstrapOptions</span></span>
<span data-ttu-id="62943-127">Specifica le opzioni di bootstrap in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="62943-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="62943-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="62943-128">-BootstrapVersion</span></span>
<span data-ttu-id="62943-129">Specifica la versione del client chef installata insieme all'estensione.</span><span class="sxs-lookup"><span data-stu-id="62943-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

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

### <span data-ttu-id="62943-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="62943-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="62943-131">Specifica la frequenza (in minuti) in cui viene eseguito il servizio chef.</span><span class="sxs-lookup"><span data-stu-id="62943-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="62943-132">Se nel caso in cui non si vuole che il servizio chef venga installato in Azure VM, impostare il valore come 0 in questo campo.</span><span class="sxs-lookup"><span data-stu-id="62943-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62943-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="62943-133">-ChefServerUrl</span></span>
<span data-ttu-id="62943-134">Specifica l'URL del server dello chef.</span><span class="sxs-lookup"><span data-stu-id="62943-134">Specifies the URL of the Chef server.</span></span>

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

### <span data-ttu-id="62943-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="62943-135">-ClientRb</span></span>
<span data-ttu-id="62943-136">Specifica il percorso completo dello chef client. RB.</span><span class="sxs-lookup"><span data-stu-id="62943-136">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="62943-137">-DAEMON</span><span class="sxs-lookup"><span data-stu-id="62943-137">-Daemon</span></span>
<span data-ttu-id="62943-138">Configura lo chef-servizio client per l'esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="62943-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="62943-139">La piattaforma node dovrebbe essere Windows.</span><span class="sxs-lookup"><span data-stu-id="62943-139">The node platform should be Windows.</span></span>
<span data-ttu-id="62943-140">Opzioni consentite: "nessuno", "servizio" e "attività".</span><span class="sxs-lookup"><span data-stu-id="62943-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="62943-141">Nessuno: al momento impedisce che il servizio chef-client venga configurato come servizio.</span><span class="sxs-lookup"><span data-stu-id="62943-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="62943-142">Service-configura lo chef-client in modo che venga eseguito automaticamente in background come servizio.</span><span class="sxs-lookup"><span data-stu-id="62943-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="62943-143">attività: configura lo chef-client in modo che venga eseguito automaticamente in background come attività secheduled.</span><span class="sxs-lookup"><span data-stu-id="62943-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="62943-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="62943-144">-InformationAction</span></span>
<span data-ttu-id="62943-145">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="62943-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="62943-146">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="62943-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62943-147">Continuare</span><span class="sxs-lookup"><span data-stu-id="62943-147">Continue</span></span>
- <span data-ttu-id="62943-148">Ignora</span><span class="sxs-lookup"><span data-stu-id="62943-148">Ignore</span></span>
- <span data-ttu-id="62943-149">Informarsi</span><span class="sxs-lookup"><span data-stu-id="62943-149">Inquire</span></span>
- <span data-ttu-id="62943-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="62943-150">SilentlyContinue</span></span>
- <span data-ttu-id="62943-151">Stop</span><span class="sxs-lookup"><span data-stu-id="62943-151">Stop</span></span>
- <span data-ttu-id="62943-152">Sospensione</span><span class="sxs-lookup"><span data-stu-id="62943-152">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62943-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="62943-153">-InformationVariable</span></span>
<span data-ttu-id="62943-154">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="62943-154">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62943-155">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="62943-155">-JsonAttribute</span></span>
<span data-ttu-id="62943-156">Una stringa JSON da aggiungere alla prima esecuzione di chef-client.</span><span class="sxs-lookup"><span data-stu-id="62943-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="62943-157">ad esempio-JsonAttribute ' {"foo": "bar"}'</span><span class="sxs-lookup"><span data-stu-id="62943-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="62943-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="62943-158">-Linux</span></span>
<span data-ttu-id="62943-159">Indica che questo cmdlet crea una macchina virtuale basata su Linux.</span><span class="sxs-lookup"><span data-stu-id="62943-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62943-160">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="62943-160">-OrganizationName</span></span>
<span data-ttu-id="62943-161">Specifica il nome dell'organizzazione dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="62943-161">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="62943-162">-Profile</span><span class="sxs-lookup"><span data-stu-id="62943-162">-Profile</span></span>
<span data-ttu-id="62943-163">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62943-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62943-164">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="62943-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62943-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="62943-165">-RunList</span></span>
<span data-ttu-id="62943-166">Specifica l'elenco di esecuzione dei nodi dello chef.</span><span class="sxs-lookup"><span data-stu-id="62943-166">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="62943-167">-Segreto</span><span class="sxs-lookup"><span data-stu-id="62943-167">-Secret</span></span>
<span data-ttu-id="62943-168">Chiave di crittografia utilizzata per crittografare e decrittografare i valori degli elementi del sacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="62943-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="62943-169">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="62943-169">-SecretFile</span></span>
<span data-ttu-id="62943-170">Percorso del file che contiene la chiave di crittografia utilizzata per crittografare e decrittografare i valori degli elementi del sacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="62943-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="62943-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="62943-171">-ValidationClientName</span></span>
<span data-ttu-id="62943-172">Specifica il nome del client di convalida.</span><span class="sxs-lookup"><span data-stu-id="62943-172">Specifies the name of the validation client.</span></span>

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

### <span data-ttu-id="62943-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="62943-173">-ValidationPem</span></span>
<span data-ttu-id="62943-174">Specifica il percorso del file validator. pem dello chef.</span><span class="sxs-lookup"><span data-stu-id="62943-174">Specifies the Chef validator .pem file path.</span></span>

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

### <span data-ttu-id="62943-175">-Versione</span><span class="sxs-lookup"><span data-stu-id="62943-175">-Version</span></span>
<span data-ttu-id="62943-176">Specifica il numero di versione dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="62943-176">Specifies the version number of the Chef extension.</span></span>

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

### <span data-ttu-id="62943-177">-VM</span><span class="sxs-lookup"><span data-stu-id="62943-177">-VM</span></span>
<span data-ttu-id="62943-178">Specifica l'oggetto macchina virtuale persistente.</span><span class="sxs-lookup"><span data-stu-id="62943-178">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62943-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="62943-179">-Windows</span></span>
<span data-ttu-id="62943-180">Indica che questo cmdlet crea una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="62943-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62943-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62943-181">CommonParameters</span></span>
<span data-ttu-id="62943-182">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62943-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62943-183">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62943-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62943-184">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62943-184">INPUTS</span></span>

## <span data-ttu-id="62943-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62943-185">OUTPUTS</span></span>

## <span data-ttu-id="62943-186">Note</span><span class="sxs-lookup"><span data-stu-id="62943-186">NOTES</span></span>

## <span data-ttu-id="62943-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62943-187">RELATED LINKS</span></span>

[<span data-ttu-id="62943-188">Get-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="62943-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="62943-189">Remove-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="62943-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


