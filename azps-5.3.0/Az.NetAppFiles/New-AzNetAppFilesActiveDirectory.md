---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474005"
---
# <span data-ttu-id="1dd64-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1dd64-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="1dd64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dd64-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd64-103">Crea una nuova configurazione di Active Directory per i file di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="1dd64-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="1dd64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dd64-104">SYNTAX</span></span>

### <span data-ttu-id="1dd64-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dd64-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd64-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dd64-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dd64-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dd64-107">DESCRIPTION</span></span>
<span data-ttu-id="1dd64-108">Il cmdlet **New-AzNetAppFilesActiveDirectory** crea una nuova configurazione di Active Directory per un account di ANF.</span><span class="sxs-lookup"><span data-stu-id="1dd64-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="1dd64-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dd64-109">EXAMPLES</span></span>

### <span data-ttu-id="1dd64-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dd64-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="1dd64-111">Questo comando consente di ottenere la password dell'annuncio da PROMT in una nuova configurazione di Active Directory per l'account ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="1dd64-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="1dd64-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dd64-112">PARAMETERS</span></span>

### <span data-ttu-id="1dd64-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1dd64-113">-AccountName</span></span>
<span data-ttu-id="1dd64-114">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="1dd64-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1dd64-115">-AccountObject</span></span>
<span data-ttu-id="1dd64-116">Account per il nuovo oggetto Criteri di backup</span><span class="sxs-lookup"><span data-stu-id="1dd64-116">The Account for the new Backup Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="1dd64-117">-AdName</span></span>
<span data-ttu-id="1dd64-118">Nome del computer di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1dd64-118">Name of the active directory machine.</span></span>
<span data-ttu-id="1dd64-119">Questo parametro facoltativo viene usato solo durante la creazione del volume Kerberos</span><span class="sxs-lookup"><span data-stu-id="1dd64-119">This optional parameter is used only while creating kerberos volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="1dd64-120">-BackupOperator</span></span>
<span data-ttu-id="1dd64-121">Utenti da aggiungere al gruppo Active Directory dell'operatore di backup predefinito.</span><span class="sxs-lookup"><span data-stu-id="1dd64-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="1dd64-122">Elenco di nomi utente univoci senza identificatore di dominio</span><span class="sxs-lookup"><span data-stu-id="1dd64-122">A list of unique usernames without domain specifier</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd64-123">-DefaultProfile</span></span>
<span data-ttu-id="1dd64-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dd64-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd64-125">-DNS</span><span class="sxs-lookup"><span data-stu-id="1dd64-125">-Dns</span></span>
<span data-ttu-id="1dd64-126">Elenco separato da virgole degli indirizzi IP del server DNS (solo IPv4) per il dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="1dd64-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-127">-Domain</span><span class="sxs-lookup"><span data-stu-id="1dd64-127">-Domain</span></span>
<span data-ttu-id="1dd64-128">Nome del dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="1dd64-128">Name of the Active Directory domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="1dd64-129">-KdcIP</span></span>
<span data-ttu-id="1dd64-130">indirizzi IP del server KDC per il computer Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1dd64-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="1dd64-131">Questo parametro facoltativo viene usato solo durante la creazione del volume Kerberos.</span><span class="sxs-lookup"><span data-stu-id="1dd64-131">This optional parameter is used only while creating kerberos volume.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="1dd64-132">-OrganizationalUnit</span></span>
<span data-ttu-id="1dd64-133">Unità organizzativa (OU) all'interno di Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="1dd64-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-134">-Password</span><span class="sxs-lookup"><span data-stu-id="1dd64-134">-Password</span></span>
<span data-ttu-id="1dd64-135">Password in formato testo normale dell'amministratore di dominio Active Directory, il valore viene mascherato nella risposta</span><span class="sxs-lookup"><span data-stu-id="1dd64-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd64-136">-ResourceGroupName</span></span>
<span data-ttu-id="1dd64-137">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="1dd64-137">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="1dd64-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="1dd64-139">Quando LDAP su SSL/TLS è abilitato, il client LDAP deve avere un certificato di CA radice autofirmato del servizio di certificazione di Active Directory con codifica Base64, questo parametro facoltativo viene usato solo per il protocollo duale con i volumi di mappatura degli utenti LDAP.</span><span class="sxs-lookup"><span data-stu-id="1dd64-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-140">-Sito</span><span class="sxs-lookup"><span data-stu-id="1dd64-140">-Site</span></span>
<span data-ttu-id="1dd64-141">Sito di Active Directory il servizio limiterà l'individuazione del controller di dominio</span><span class="sxs-lookup"><span data-stu-id="1dd64-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="1dd64-142">-SmbServerName</span></span>
<span data-ttu-id="1dd64-143">Nome NetBIOS del server SMB.</span><span class="sxs-lookup"><span data-stu-id="1dd64-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="1dd64-144">Questo nome verrà registrato come account di computer nell'annuncio e usato per montare i volumi</span><span class="sxs-lookup"><span data-stu-id="1dd64-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-145">-Username</span><span class="sxs-lookup"><span data-stu-id="1dd64-145">-Username</span></span>
<span data-ttu-id="1dd64-146">Nome utente dell'amministratore di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="1dd64-146">Username of Active Directory domain administrator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dd64-147">-Confirm</span></span>
<span data-ttu-id="1dd64-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dd64-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd64-149">-WhatIf</span></span>
<span data-ttu-id="1dd64-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dd64-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd64-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dd64-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd64-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd64-152">CommonParameters</span></span>
<span data-ttu-id="1dd64-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd64-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd64-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dd64-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd64-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dd64-155">INPUTS</span></span>

### <span data-ttu-id="1dd64-156">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1dd64-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1dd64-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dd64-157">OUTPUTS</span></span>

### <span data-ttu-id="1dd64-158">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1dd64-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="1dd64-159">Note</span><span class="sxs-lookup"><span data-stu-id="1dd64-159">NOTES</span></span>

## <span data-ttu-id="1dd64-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dd64-160">RELATED LINKS</span></span>
