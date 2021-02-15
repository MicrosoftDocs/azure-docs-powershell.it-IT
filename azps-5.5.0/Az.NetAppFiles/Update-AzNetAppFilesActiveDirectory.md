---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203288"
---
# <span data-ttu-id="682f0-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="682f0-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="682f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="682f0-102">SYNOPSIS</span></span>
<span data-ttu-id="682f0-103">Aggiorna la configurazione di Active Directory Azure NetApp Files (ANF) ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="682f0-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="682f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="682f0-104">SYNTAX</span></span>

### <span data-ttu-id="682f0-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="682f0-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="682f0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="682f0-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="682f0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="682f0-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="682f0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="682f0-108">DESCRIPTION</span></span>
<span data-ttu-id="682f0-109">Il cmdlet **Update-AzNetAppFilesAccount** modifica una configurazione di Active Directory ANF.</span><span class="sxs-lookup"><span data-stu-id="682f0-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="682f0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="682f0-110">EXAMPLES</span></span>

### <span data-ttu-id="682f0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="682f0-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="682f0-112">Questo comando esegue un aggiornamento sulla configurazione di Active Directory specificata modificando il nome utente specificato.</span><span class="sxs-lookup"><span data-stu-id="682f0-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="682f0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="682f0-113">PARAMETERS</span></span>

### <span data-ttu-id="682f0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="682f0-114">-AccountName</span></span>
<span data-ttu-id="682f0-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="682f0-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="682f0-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="682f0-116">-AccountObject</span></span>
<span data-ttu-id="682f0-117">Account per l'oggetto Active Directory</span><span class="sxs-lookup"><span data-stu-id="682f0-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="682f0-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="682f0-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="682f0-119">ID della directory attiva ANF</span><span class="sxs-lookup"><span data-stu-id="682f0-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682f0-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="682f0-120">-AdName</span></span>
<span data-ttu-id="682f0-121">Nome del computer Active Directory.</span><span class="sxs-lookup"><span data-stu-id="682f0-121">Name of the active directory machine.</span></span>
<span data-ttu-id="682f0-122">Questo parametro facoltativo viene usato solo durante la creazione del volume Kerberos</span><span class="sxs-lookup"><span data-stu-id="682f0-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="682f0-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="682f0-123">-BackupOperator</span></span>
<span data-ttu-id="682f0-124">Utenti da aggiungere al gruppo Active Directory Operator di backup predefinito.</span><span class="sxs-lookup"><span data-stu-id="682f0-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="682f0-125">Elenco di nomi utente univoci senza specificatore di dominio</span><span class="sxs-lookup"><span data-stu-id="682f0-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="682f0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="682f0-126">-DefaultProfile</span></span>
<span data-ttu-id="682f0-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="682f0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="682f0-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="682f0-128">-Dns</span></span>
<span data-ttu-id="682f0-129">Elenco separato da virgola degli indirizzi IP del server DNS (solo IPv4) per il dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="682f0-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="682f0-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="682f0-130">-Domain</span></span>
<span data-ttu-id="682f0-131">Nome del dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="682f0-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="682f0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="682f0-132">-InputObject</span></span>
<span data-ttu-id="682f0-133">L'oggetto Active Directory da rimuovere</span><span class="sxs-lookup"><span data-stu-id="682f0-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="682f0-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="682f0-134">-KdcIP</span></span>
<span data-ttu-id="682f0-135">Indirizzi IP del server kdc per il computer Active Directory.</span><span class="sxs-lookup"><span data-stu-id="682f0-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="682f0-136">Questo parametro facoltativo viene usato solo durante la creazione del volume Kerberos.</span><span class="sxs-lookup"><span data-stu-id="682f0-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="682f0-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="682f0-137">-OrganizationalUnit</span></span>
<span data-ttu-id="682f0-138">Unità organizzativa all'interno di Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="682f0-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="682f0-139">-Password</span><span class="sxs-lookup"><span data-stu-id="682f0-139">-Password</span></span>
<span data-ttu-id="682f0-140">Password in testo normale dell'amministratore di dominio Active Directory. Il valore è mascherato nella risposta</span><span class="sxs-lookup"><span data-stu-id="682f0-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="682f0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="682f0-141">-ResourceGroupName</span></span>
<span data-ttu-id="682f0-142">Gruppo di risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="682f0-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="682f0-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="682f0-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="682f0-144">Quando ldap su SSL/TLS è abilitato, è necessario che il client LDAP abbia il certificato CA radice autofirmato di Active Directory Certificate Service codificato in base64, questo parametro facoltativo viene usato solo per il dual protocol con volumi di mapping degli utenti LDAP.</span><span class="sxs-lookup"><span data-stu-id="682f0-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="682f0-145">-Site</span><span class="sxs-lookup"><span data-stu-id="682f0-145">-Site</span></span>
<span data-ttu-id="682f0-146">Il sito di Active Directory a cui il servizio limiterà l'individuazione del controller di dominio</span><span class="sxs-lookup"><span data-stu-id="682f0-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="682f0-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="682f0-147">-SmbServerName</span></span>
<span data-ttu-id="682f0-148">Nome Net PIÙ.SE del server SMB.</span><span class="sxs-lookup"><span data-stu-id="682f0-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="682f0-149">Questo nome verrà registrato come account del computer in Active Directory e usato per il montaggio di volumi</span><span class="sxs-lookup"><span data-stu-id="682f0-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="682f0-150">-Username</span><span class="sxs-lookup"><span data-stu-id="682f0-150">-Username</span></span>
<span data-ttu-id="682f0-151">Nome utente dell'amministratore di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="682f0-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="682f0-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="682f0-152">-Confirm</span></span>
<span data-ttu-id="682f0-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="682f0-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="682f0-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="682f0-154">-WhatIf</span></span>
<span data-ttu-id="682f0-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="682f0-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="682f0-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="682f0-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="682f0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="682f0-157">CommonParameters</span></span>
<span data-ttu-id="682f0-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="682f0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="682f0-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="682f0-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="682f0-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="682f0-160">INPUTS</span></span>

### <span data-ttu-id="682f0-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="682f0-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="682f0-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="682f0-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="682f0-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="682f0-163">OUTPUTS</span></span>

### <span data-ttu-id="682f0-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="682f0-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="682f0-165">NOTE</span><span class="sxs-lookup"><span data-stu-id="682f0-165">NOTES</span></span>

## <span data-ttu-id="682f0-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="682f0-166">RELATED LINKS</span></span>
