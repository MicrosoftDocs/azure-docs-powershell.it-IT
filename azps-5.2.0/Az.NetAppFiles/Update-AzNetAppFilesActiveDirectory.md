---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335320"
---
# <span data-ttu-id="d7437-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d7437-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="d7437-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7437-102">SYNOPSIS</span></span>
<span data-ttu-id="d7437-103">Aggiorna una configurazione di Active Directory dei file di Azure NetApp (ANF) ai modificatori facoltativi forniti.</span><span class="sxs-lookup"><span data-stu-id="d7437-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="d7437-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7437-104">SYNTAX</span></span>

### <span data-ttu-id="d7437-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7437-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7437-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7437-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7437-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7437-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7437-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7437-108">DESCRIPTION</span></span>
<span data-ttu-id="d7437-109">Il cmdlet **Update-AzNetAppFilesAccount** modifica una configurazione di Active Directory di ANF.</span><span class="sxs-lookup"><span data-stu-id="d7437-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="d7437-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7437-110">EXAMPLES</span></span>

### <span data-ttu-id="d7437-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d7437-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="d7437-112">Questo comando esegue un aggiornamento nella configurazione di Active Directory specificata modificando il nome utente in quello fornito.</span><span class="sxs-lookup"><span data-stu-id="d7437-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="d7437-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7437-113">PARAMETERS</span></span>

### <span data-ttu-id="d7437-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7437-114">-AccountName</span></span>
<span data-ttu-id="d7437-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="d7437-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="d7437-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="d7437-116">-AccountObject</span></span>
<span data-ttu-id="d7437-117">Account per l'oggetto Active Directory</span><span class="sxs-lookup"><span data-stu-id="d7437-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="d7437-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="d7437-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="d7437-119">ID della ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="d7437-119">The ID of the ANF active directory</span></span>

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

### <span data-ttu-id="d7437-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="d7437-120">-AdName</span></span>
<span data-ttu-id="d7437-121">Nome del computer di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d7437-121">Name of the active directory machine.</span></span>
<span data-ttu-id="d7437-122">Questo parametro facoltativo viene usato solo durante la creazione del volume Kerberos</span><span class="sxs-lookup"><span data-stu-id="d7437-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="d7437-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="d7437-123">-BackupOperator</span></span>
<span data-ttu-id="d7437-124">Utenti da aggiungere al gruppo Active Directory dell'operatore di backup predefinito.</span><span class="sxs-lookup"><span data-stu-id="d7437-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="d7437-125">Elenco di nomi utente univoci senza identificatore di dominio</span><span class="sxs-lookup"><span data-stu-id="d7437-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="d7437-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7437-126">-DefaultProfile</span></span>
<span data-ttu-id="d7437-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7437-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7437-128">-DNS</span><span class="sxs-lookup"><span data-stu-id="d7437-128">-Dns</span></span>
<span data-ttu-id="d7437-129">Elenco separato da virgole degli indirizzi IP del server DNS (solo IPv4) per il dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="d7437-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="d7437-130">-Domain</span><span class="sxs-lookup"><span data-stu-id="d7437-130">-Domain</span></span>
<span data-ttu-id="d7437-131">Nome del dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="d7437-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="d7437-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7437-132">-InputObject</span></span>
<span data-ttu-id="d7437-133">Oggetto Active Directory da rimuovere</span><span class="sxs-lookup"><span data-stu-id="d7437-133">The active directory object to remove</span></span>

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

### <span data-ttu-id="d7437-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="d7437-134">-KdcIP</span></span>
<span data-ttu-id="d7437-135">indirizzi IP del server KDC per il computer Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d7437-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="d7437-136">Questo parametro facoltativo viene usato solo durante la creazione del volume Kerberos.</span><span class="sxs-lookup"><span data-stu-id="d7437-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="d7437-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="d7437-137">-OrganizationalUnit</span></span>
<span data-ttu-id="d7437-138">Unità organizzativa (OU) all'interno di Windows Active Directory</span><span class="sxs-lookup"><span data-stu-id="d7437-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="d7437-139">-Password</span><span class="sxs-lookup"><span data-stu-id="d7437-139">-Password</span></span>
<span data-ttu-id="d7437-140">Password in formato testo normale dell'amministratore di dominio Active Directory, il valore viene mascherato nella risposta</span><span class="sxs-lookup"><span data-stu-id="d7437-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="d7437-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7437-141">-ResourceGroupName</span></span>
<span data-ttu-id="d7437-142">Gruppo risorse dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="d7437-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d7437-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="d7437-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="d7437-144">Quando LDAP su SSL/TLS è abilitato, il client LDAP deve avere un certificato di CA radice autofirmato del servizio di certificazione di Active Directory con codifica Base64, questo parametro facoltativo viene usato solo per il protocollo duale con i volumi di mappatura degli utenti LDAP.</span><span class="sxs-lookup"><span data-stu-id="d7437-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="d7437-145">-Sito</span><span class="sxs-lookup"><span data-stu-id="d7437-145">-Site</span></span>
<span data-ttu-id="d7437-146">Sito di Active Directory il servizio limiterà l'individuazione del controller di dominio</span><span class="sxs-lookup"><span data-stu-id="d7437-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="d7437-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="d7437-147">-SmbServerName</span></span>
<span data-ttu-id="d7437-148">Nome NetBIOS del server SMB.</span><span class="sxs-lookup"><span data-stu-id="d7437-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="d7437-149">Questo nome verrà registrato come account di computer nell'annuncio e usato per montare i volumi</span><span class="sxs-lookup"><span data-stu-id="d7437-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="d7437-150">-Username</span><span class="sxs-lookup"><span data-stu-id="d7437-150">-Username</span></span>
<span data-ttu-id="d7437-151">Nome utente dell'amministratore di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="d7437-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="d7437-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d7437-152">-Confirm</span></span>
<span data-ttu-id="d7437-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7437-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7437-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7437-154">-WhatIf</span></span>
<span data-ttu-id="d7437-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7437-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7437-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7437-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7437-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7437-157">CommonParameters</span></span>
<span data-ttu-id="d7437-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7437-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7437-159">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7437-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7437-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7437-160">INPUTS</span></span>

### <span data-ttu-id="d7437-161">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d7437-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="d7437-162">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d7437-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="d7437-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7437-163">OUTPUTS</span></span>

### <span data-ttu-id="d7437-164">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="d7437-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="d7437-165">Note</span><span class="sxs-lookup"><span data-stu-id="d7437-165">NOTES</span></span>

## <span data-ttu-id="d7437-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7437-166">RELATED LINKS</span></span>
