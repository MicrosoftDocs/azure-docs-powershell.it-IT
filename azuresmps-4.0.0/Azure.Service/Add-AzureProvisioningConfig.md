---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029844"
---
# <span data-ttu-id="b5fc5-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="b5fc5-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="b5fc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5fc5-103">Aggiunge la configurazione di provisioning per una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="b5fc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5fc5-104">SYNTAX</span></span>

### <span data-ttu-id="b5fc5-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5fc5-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b5fc5-106">Linux</span><span class="sxs-lookup"><span data-stu-id="b5fc5-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b5fc5-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="b5fc5-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5fc5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5fc5-108">DESCRIPTION</span></span>
<span data-ttu-id="b5fc5-109">Il cmdlet **Add-AzureProvisioningConfig** aggiunge le informazioni di configurazione di provisioning a una configurazione di una macchina virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="b5fc5-110">Puoi usare l'oggetto Configuration per creare una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="b5fc5-111">Questo cmdlet supporta diverse configurazioni di provisioning, inclusi i server Windows autonomi, i server Windows collegati a un dominio Active Directory e i server basati su Linux.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="b5fc5-112">Per creare un server di dominio Active Directory, specificare il nome di dominio completo del dominio Active Directory e le credenziali del dominio di un utente che disponga delle autorizzazioni necessarie per accedere alla macchina virtuale al dominio.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="b5fc5-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5fc5-113">EXAMPLES</span></span>

### <span data-ttu-id="b5fc5-114">Esempio 1: creare una macchina virtuale autonoma</span><span class="sxs-lookup"><span data-stu-id="b5fc5-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="b5fc5-115">Questo comando crea un oggetto di configurazione della macchina virtuale usando il cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="b5fc5-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="b5fc5-116">Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b5fc5-117">Il cmdlet corrente aggiunge la configurazione di provisioning per una macchina virtuale che esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="b5fc5-118">La configurazione include il nome utente e la password di amministratore.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="b5fc5-119">Il comando passa la configurazione al cmdlet **New-AzureVM** , che crea la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="b5fc5-120">Esempio 2: creare una macchina virtuale collegata a un dominio</span><span class="sxs-lookup"><span data-stu-id="b5fc5-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="b5fc5-121">Questo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5fc5-122">Il cmdlet corrente aggiunge la configurazione di provisioning per una macchina virtuale da unire al dominio contoso.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="b5fc5-123">Il comando include il nome utente e la password necessari per accedere alla macchina virtuale al dominio.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="b5fc5-124">La configurazione richiede all'utente di cambiare la password dell'utente al primo accesso.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="b5fc5-125">Il comando crea la macchina virtuale in base all'oggetto provisioning.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5fc5-126">Esempio 3: creare una macchina virtuale basata su Linux</span><span class="sxs-lookup"><span data-stu-id="b5fc5-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="b5fc5-127">Questo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5fc5-128">Il cmdlet corrente aggiunge la configurazione di provisioning per una macchina virtuale che esegue il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="b5fc5-129">La configurazione include il nome utente e la password radice.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="b5fc5-130">Il comando crea la macchina virtuale in base all'oggetto provisioning.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5fc5-131">Esempio 4: creare una macchina virtuale che include i certificati per WinRM</span><span class="sxs-lookup"><span data-stu-id="b5fc5-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="b5fc5-132">Il primo comando ottiene i certificati da un archivio certificati e li archivia nella variabile di matrice $certs.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="b5fc5-133">Il secondo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5fc5-134">Il cmdlet corrente aggiunge la configurazione di provisioning che include i certificati per WinRM.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="b5fc5-135">Il comando crea la macchina virtuale in base all'oggetto provisioning.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5fc5-136">Esempio 5: creare una macchina virtuale con WinRM abilitato tramite HTTP</span><span class="sxs-lookup"><span data-stu-id="b5fc5-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="b5fc5-137">Questo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5fc5-138">Il cmdlet corrente aggiunge la configurazione di provisioning con WinRM abilitato tramite HTTP.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="b5fc5-139">Il comando crea la macchina virtuale in base all'oggetto provisioning.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5fc5-140">Esempio 6: creare una macchina virtuale con WinRM disabilitato tramite HTTPS</span><span class="sxs-lookup"><span data-stu-id="b5fc5-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="b5fc5-141">Questo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5fc5-142">Il cmdlet corrente aggiunge la configurazione di provisioning che disattiva WinRM tramite HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="b5fc5-143">Il comando crea la macchina virtuale in base all'oggetto provisioning.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="b5fc5-144">Esempio 7: creare una macchina virtuale senza esportare i tasti</span><span class="sxs-lookup"><span data-stu-id="b5fc5-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="b5fc5-145">Il primo comando ottiene i certificati da un archivio certificati e li archivia nella variabile di matrice $certs.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="b5fc5-146">Il secondo comando crea un oggetto di configurazione della macchina virtuale e lo passa al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="b5fc5-147">Il cmdlet corrente aggiunge la configurazione di provisioning per una macchina virtuale che include i certificati e non Esporta le chiavi private.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="b5fc5-148">Il comando crea la macchina virtuale in base all'oggetto provisioning.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="b5fc5-149">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5fc5-149">PARAMETERS</span></span>

### <span data-ttu-id="b5fc5-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="b5fc5-150">-AdminUsername</span></span>
<span data-ttu-id="b5fc5-151">Specifica il nome utente dell'account di amministratore creato dalla configurazione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-152">-Certificati</span><span class="sxs-lookup"><span data-stu-id="b5fc5-152">-Certificates</span></span>
<span data-ttu-id="b5fc5-153">Specifica un set di certificati installati dalla configurazione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-154">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="b5fc5-154">-CustomDataFile</span></span>
<span data-ttu-id="b5fc5-155">Specifica un file di dati per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="b5fc5-156">Questo cmdlet codifica il contenuto del file come Base64.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="b5fc5-157">Il file deve essere di lunghezza inferiore a 64 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="b5fc5-158">Se il sistema operativo guest è il sistema operativo Windows, questa configurazione salva questi dati come file binario denominato%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="b5fc5-159">Se il sistema operativo guest è Linux, questa configurazione passa i dati usando il file ovf-env.xml.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="b5fc5-160">La configurazione copia il file nella directory/var/lib/waagent.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="b5fc5-161">L'agente archivia anche i dati codificati base64 in/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="b5fc5-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="b5fc5-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="b5fc5-163">Indica che questa configurazione Disabilita gli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="b5fc5-164">-DisableGuestAgent</span></span>
<span data-ttu-id="b5fc5-165">Indica che questa configurazione Disabilita l'agente guest dell'infrastruttura come servizio (IaaS).</span><span class="sxs-lookup"><span data-stu-id="b5fc5-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="b5fc5-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="b5fc5-166">-DisableSSH</span></span>
<span data-ttu-id="b5fc5-167">Indica che questa configurazione Disabilita SSH.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="b5fc5-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="b5fc5-169">Indica che questa configurazione Disabilita Windows Remote Management (WinRM) in HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="b5fc5-170">Per impostazione predefinita, WinRM è abilitato su HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-171">-Domain</span><span class="sxs-lookup"><span data-stu-id="b5fc5-171">-Domain</span></span>
<span data-ttu-id="b5fc5-172">Specifica il nome del dominio dell'account con l'autorizzazione per aggiungere il computer a un dominio.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="b5fc5-173">-DomainPassword</span></span>
<span data-ttu-id="b5fc5-174">Specifica la password dell'account utente con l'autorizzazione per aggiungere il computer a un dominio.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="b5fc5-175">-DomainUserName</span></span>
<span data-ttu-id="b5fc5-176">Specifica il nome dell'account utente che dispone delle autorizzazioni per aggiungere il computer a un dominio.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="b5fc5-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="b5fc5-178">Indica che questa configurazione Abilita WinRM su HTTP.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-179">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b5fc5-179">-InformationAction</span></span>
<span data-ttu-id="b5fc5-180">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5fc5-181">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5fc5-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5fc5-182">Continuare</span><span class="sxs-lookup"><span data-stu-id="b5fc5-182">Continue</span></span>
- <span data-ttu-id="b5fc5-183">Ignora</span><span class="sxs-lookup"><span data-stu-id="b5fc5-183">Ignore</span></span>
- <span data-ttu-id="b5fc5-184">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b5fc5-184">Inquire</span></span>
- <span data-ttu-id="b5fc5-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5fc5-185">SilentlyContinue</span></span>
- <span data-ttu-id="b5fc5-186">Stop</span><span class="sxs-lookup"><span data-stu-id="b5fc5-186">Stop</span></span>
- <span data-ttu-id="b5fc5-187">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b5fc5-187">Suspend</span></span>

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

### <span data-ttu-id="b5fc5-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5fc5-188">-InformationVariable</span></span>
<span data-ttu-id="b5fc5-189">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-189">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5fc5-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="b5fc5-190">-JoinDomain</span></span>
<span data-ttu-id="b5fc5-191">Specifica il nome di dominio completo (FQDN) del dominio a cui partecipare.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="b5fc5-192">-Linux</span></span>
<span data-ttu-id="b5fc5-193">Indica che questa configurazione crea una configurazione Linux.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-193">Indicates that this configuration creates a Linux configuration.</span></span>

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

### <span data-ttu-id="b5fc5-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="b5fc5-194">-LinuxUser</span></span>
<span data-ttu-id="b5fc5-195">Specifica il nome utente dell'account amministrativo di Linux creato dalla configurazione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="b5fc5-196">-MachineObjectOU</span></span>
<span data-ttu-id="b5fc5-197">Specifica il nome completo dell'unità organizzativa in cui la configurazione crea l'account del computer.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="b5fc5-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="b5fc5-199">Indica che questa configurazione non carica la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5fc5-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="b5fc5-201">Indica che questa configurazione crea una macchina virtuale senza un endpoint desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5fc5-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="b5fc5-203">Indica che questa configurazione crea una macchina virtuale senza un endpoint SSH.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="b5fc5-204">-NoSSHPassword</span></span>
<span data-ttu-id="b5fc5-205">Indica che questa configurazione crea una macchina virtuale senza una password SSH.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b5fc5-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="b5fc5-207">Indica che questa configurazione non aggiunge un endpoint di WinRM per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-208">-Password</span><span class="sxs-lookup"><span data-stu-id="b5fc5-208">-Password</span></span>
<span data-ttu-id="b5fc5-209">Specifica la password dell'account di amministratore.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-209">Specifies the password of the administrator account.</span></span>

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

### <span data-ttu-id="b5fc5-210">-Profile</span><span class="sxs-lookup"><span data-stu-id="b5fc5-210">-Profile</span></span>
<span data-ttu-id="b5fc5-211">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5fc5-212">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5fc5-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="b5fc5-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="b5fc5-214">Indica che la macchina virtuale richiede all'utente di cambiare la password al primo accesso.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="b5fc5-215">-SSHKeyPairs</span></span>
<span data-ttu-id="b5fc5-216">Specifica le coppie di chiavi SSH.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-216">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="b5fc5-217">-SSHPublicKeys</span></span>
<span data-ttu-id="b5fc5-218">Specifica le chiavi pubbliche di SSH.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-218">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-219">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="b5fc5-219">-TimeZone</span></span>
<span data-ttu-id="b5fc5-220">Specifica il fuso orario per la macchina virtuale, ad esempio ora solare Pacifico o ora solare fuso centrale Canada.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-221">-VM</span><span class="sxs-lookup"><span data-stu-id="b5fc5-221">-VM</span></span>
<span data-ttu-id="b5fc5-222">Specifica un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="b5fc5-223">-Windows</span></span>
<span data-ttu-id="b5fc5-224">Indica che questa configurazione crea una macchina virtuale autonoma che esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

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

### <span data-ttu-id="b5fc5-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="b5fc5-225">-WindowsDomain</span></span>
<span data-ttu-id="b5fc5-226">Indica che questa configurazione crea Windows Server aggiunto a un dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="b5fc5-227">-WinRMCertificate</span></span>
<span data-ttu-id="b5fc5-228">Specifica un certificato che questa configurazione associa a un endpoint di WinRM.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="b5fc5-229">-X509Certificates</span></span>
<span data-ttu-id="b5fc5-230">Specifica una matrice di certificati X509 distribuiti in un servizio ospitato.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5fc5-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5fc5-231">CommonParameters</span></span>
<span data-ttu-id="b5fc5-232">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5fc5-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5fc5-233">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5fc5-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5fc5-234">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5fc5-234">INPUTS</span></span>

## <span data-ttu-id="b5fc5-235">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5fc5-235">OUTPUTS</span></span>

## <span data-ttu-id="b5fc5-236">Note</span><span class="sxs-lookup"><span data-stu-id="b5fc5-236">NOTES</span></span>

## <span data-ttu-id="b5fc5-237">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5fc5-237">RELATED LINKS</span></span>

[<span data-ttu-id="b5fc5-238">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b5fc5-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="b5fc5-239">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="b5fc5-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


