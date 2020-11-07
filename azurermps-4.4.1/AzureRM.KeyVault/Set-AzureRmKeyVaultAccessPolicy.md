---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://go.microsoft.com/fwlink/?LinkId=690163
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 9ebf606a41a3a972b2d636846fbdc7834388ef29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521212"
---
# <span data-ttu-id="8072b-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8072b-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="8072b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8072b-102">SYNOPSIS</span></span>
<span data-ttu-id="8072b-103">Concede o modifica le autorizzazioni esistenti per un utente, un'applicazione o un gruppo di sicurezza per eseguire operazioni con un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8072b-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8072b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8072b-104">SYNTAX</span></span>

### <span data-ttu-id="8072b-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8072b-105">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8072b-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8072b-106">ByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8072b-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="8072b-107">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8072b-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8072b-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8072b-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="8072b-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8072b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8072b-110">DESCRIPTION</span></span>
<span data-ttu-id="8072b-111">Il cmdlet **set-AzureRmKeyVaultAccessPolicy** concede o modifica le autorizzazioni esistenti per un utente, un'applicazione o un gruppo di sicurezza per eseguire le operazioni specificate con un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8072b-111">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span>
<span data-ttu-id="8072b-112">Non modifica le autorizzazioni di altri utenti, applicazioni o gruppi di sicurezza nel Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8072b-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="8072b-113">Se si stanno impostando le autorizzazioni per un gruppo di sicurezza, questa operazione interessa solo gli utenti del gruppo di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8072b-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="8072b-114">Le directory seguenti devono essere tutte della stessa directory di Azure:</span><span class="sxs-lookup"><span data-stu-id="8072b-114">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="8072b-115">Directory predefinita dell'abbonamento a Azure in cui si trova il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8072b-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="8072b-116">Directory di Azure che contiene l'utente o il gruppo di applicazioni a cui si stanno concedendo le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="8072b-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="8072b-117">Esempi di scenari in cui queste condizioni non vengono soddisfatte e questo cmdlet non funziona:</span><span class="sxs-lookup"><span data-stu-id="8072b-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="8072b-118">Autorizzazione di un utente di un'organizzazione diversa per gestire il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8072b-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="8072b-119">Ogni organizzazione ha una propria directory.</span><span class="sxs-lookup"><span data-stu-id="8072b-119">Each organization has its own directory.</span></span> 
- <span data-ttu-id="8072b-120">L'account di Azure include più directory.</span><span class="sxs-lookup"><span data-stu-id="8072b-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="8072b-121">Se si registra un'applicazione in una directory diversa da quella predefinita, non è possibile autorizzare l'applicazione a usare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8072b-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="8072b-122">L'applicazione deve essere nella directory predefinita.</span><span class="sxs-lookup"><span data-stu-id="8072b-122">The application must be in the default directory.</span></span>

<span data-ttu-id="8072b-123">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, devi farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8072b-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="8072b-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8072b-124">EXAMPLES</span></span>

### <span data-ttu-id="8072b-125">Esempio 1: concedere le autorizzazioni a un utente per un Vault Key Vault Key e modificare il Vault di permissionskey</span><span class="sxs-lookup"><span data-stu-id="8072b-125">Example 1: Grant permissions to a user for a key vault Key Vault and modify the permissionskey vault</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets 'set,delete'
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="8072b-126">Il primo comando concede le autorizzazioni per un utente in Azure Active Directory, PattiFuller@contoso.com per eseguire operazioni su chiavi e segreti con un Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8072b-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="8072b-127">Il secondo comando modifica le autorizzazioni concesse al PattiFuller@contoso.com primo comando per consentire l'ottenimento di segreti oltre a impostarli ed eliminarli.</span><span class="sxs-lookup"><span data-stu-id="8072b-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span>
<span data-ttu-id="8072b-128">Le autorizzazioni per le operazioni chiave restano invariate dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="8072b-128">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="8072b-129">Il parametro *PassThru* genera l'oggetto updated restituito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8072b-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="8072b-130">Il comando finale modifica ulteriormente le autorizzazioni esistenti per PattiFuller@contoso.com rimuovere tutte le autorizzazioni per le operazioni principali.</span><span class="sxs-lookup"><span data-stu-id="8072b-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span>
<span data-ttu-id="8072b-131">Le autorizzazioni per le operazioni segrete restano invariate dopo questo comando.</span><span class="sxs-lookup"><span data-stu-id="8072b-131">The permissions to secret operations remain unchanged after this command.</span></span>
<span data-ttu-id="8072b-132">Il parametro *PassThru* genera l'oggetto updated restituito dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8072b-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="8072b-133">Esempio 2: concedere le autorizzazioni per un'entità del servizio applicazione per la lettura e la scrittura di segreti</span><span class="sxs-lookup"><span data-stu-id="8072b-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="8072b-134">Questo comando consente di concedere le autorizzazioni per un'applicazione per un Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8072b-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8072b-135">Il parametro *servicePrincipalName* specifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8072b-135">The *ServicePrincipalName* parameter specifies the application.</span></span>
<span data-ttu-id="8072b-136">L'applicazione deve essere registrata in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8072b-136">The application must be registered in your Azure Active Directory.</span></span>
<span data-ttu-id="8072b-137">Il valore del parametro *servicePrincipalName* deve essere il nome dell'entità servizio dell'applicazione o il GUID dell'ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="8072b-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="8072b-138">Questo esempio specifica il nome dell'entità servizio http://payroll.contoso.com e il comando concede alle autorizzazioni dell'applicazione la lettura e la scrittura dei segreti.</span><span class="sxs-lookup"><span data-stu-id="8072b-138">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="8072b-139">Esempio 3: concedere le autorizzazioni per un'applicazione usando il relativo ID oggetto</span><span class="sxs-lookup"><span data-stu-id="8072b-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="8072b-140">Questo comando concede alle autorizzazioni dell'applicazione la lettura e la scrittura di segreti.</span><span class="sxs-lookup"><span data-stu-id="8072b-140">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="8072b-141">Questo esempio specifica l'applicazione che usa l'ID oggetto dell'entità servizio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8072b-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="8072b-142">Esempio 4: concedere le autorizzazioni per un nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="8072b-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="8072b-143">Questo comando consente di concedere le autorizzazioni Get, List e set per il nome dell'entità utente specificato per l'accesso ai segreti.</span><span class="sxs-lookup"><span data-stu-id="8072b-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="8072b-144">Esempio 5: abilitare i segreti per essere recuperati da un Vault chiave da Microsoft. Compute Resource providerkey Vault</span><span class="sxs-lookup"><span data-stu-id="8072b-144">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource providerkey vault</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="8072b-145">Questo comando concede le autorizzazioni per i segreti da recuperare dall'archivio della chiave Contoso03Vault dal provider di risorse Microsoft. Compute.</span><span class="sxs-lookup"><span data-stu-id="8072b-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="8072b-146">Esempio 6: concedere le autorizzazioni a un gruppo di sicurezza</span><span class="sxs-lookup"><span data-stu-id="8072b-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="8072b-147">Il primo comando usa il cmdlet Get-AzureRmADGroup per ottenere tutti i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8072b-147">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span>
<span data-ttu-id="8072b-148">Nell'output vengono visualizzati 3 gruppi restituiti, denominati **Group1** , **group2** e **Group3**.</span><span class="sxs-lookup"><span data-stu-id="8072b-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span>
<span data-ttu-id="8072b-149">Più gruppi possono avere lo stesso nome, ma hanno sempre un ObjectId univoco.</span><span class="sxs-lookup"><span data-stu-id="8072b-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span>
<span data-ttu-id="8072b-150">Quando viene restituito più di un gruppo con lo stesso nome, usare il parametro ObjectId nell'output per identificare quello che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="8072b-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="8072b-151">Si usa quindi l'output di questo comando con Set-AzureRmKeyVaultAccessPolicy per concedere le autorizzazioni a group2 per il Vault chiave, denominato **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="8072b-151">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span>
<span data-ttu-id="8072b-152">Questo esempio enumera i gruppi denominati "group2" inline nella stessa riga di comando.</span><span class="sxs-lookup"><span data-stu-id="8072b-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="8072b-153">Nell'elenco restituito possono essere presenti più gruppi denominati "group2".</span><span class="sxs-lookup"><span data-stu-id="8072b-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="8072b-154">Questo esempio seleziona il primo, indicato dall'indice \[ 0 \] nell'elenco restituito.</span><span class="sxs-lookup"><span data-stu-id="8072b-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="8072b-155">Esempio 7: concedere ad Azure Information Protection Access alla chiave tenant gestita dal cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="8072b-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,encrypt,unwrapkey,wrapkey,verify,sign,get
```

<span data-ttu-id="8072b-156">Questo comando autorizza Azure Information Protection a usare una chiave gestita dal cliente (la chiave Bring your own o "BYOK") come chiave del tenant di Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="8072b-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="8072b-157">Quando si esegue questo comando, specificare il proprio nome del Vault, ma è necessario specificare il parametro *servicePrincipalName* con il GUID **00000012-0000-0000-C000-000000000000** e specificare tutte le autorizzazioni nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="8072b-157">When you run this command, specify your own vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify all the permissions in the example.</span></span>

## <span data-ttu-id="8072b-158">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8072b-158">PARAMETERS</span></span>

### <span data-ttu-id="8072b-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8072b-159">-ApplicationId</span></span>
<span data-ttu-id="8072b-160">Per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8072b-160">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-161">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="8072b-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="8072b-162">Consente di specificare un ID oggetto senza convalidare che l'oggetto esiste in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8072b-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="8072b-163">Usare questo parametro solo se si vuole concedere l'accesso al Vault della chiave a un ID oggetto che fa riferimento a un gruppo di sicurezza delegata di un altro tenant Azure.</span><span class="sxs-lookup"><span data-stu-id="8072b-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-164">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8072b-164">-EmailAddress</span></span>
<span data-ttu-id="8072b-165">Specifica l'indirizzo di posta elettronica dell'utente a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="8072b-165">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="8072b-166">Questo indirizzo di posta elettronica deve esistere nella directory associata alla sottoscrizione corrente ed essere univoco.</span><span class="sxs-lookup"><span data-stu-id="8072b-166">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-167">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="8072b-167">-EnabledForDeployment</span></span>
<span data-ttu-id="8072b-168">Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8072b-168">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-169">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8072b-169">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="8072b-170">Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="8072b-170">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-171">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="8072b-171">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="8072b-172">Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="8072b-172">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-173">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8072b-173">-ObjectId</span></span>
<span data-ttu-id="8072b-174">Specifica l'ID oggetto dell'entità di servizio o dell'utente in Azure Active Directory per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="8072b-174">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-175">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8072b-175">-PassThru</span></span>
<span data-ttu-id="8072b-176">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8072b-176">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8072b-177">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8072b-177">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8072b-178">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="8072b-178">-PermissionsToCertificates</span></span>
<span data-ttu-id="8072b-179">Specifica una matrice di autorizzazioni di certificato da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="8072b-179">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8072b-180">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8072b-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8072b-181">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8072b-181">Get</span></span>
- <span data-ttu-id="8072b-182">Elenco</span><span class="sxs-lookup"><span data-stu-id="8072b-182">List</span></span>
- <span data-ttu-id="8072b-183">Eliminare</span><span class="sxs-lookup"><span data-stu-id="8072b-183">Delete</span></span>
- <span data-ttu-id="8072b-184">Creare</span><span class="sxs-lookup"><span data-stu-id="8072b-184">Create</span></span>
- <span data-ttu-id="8072b-185">Importazione</span><span class="sxs-lookup"><span data-stu-id="8072b-185">Import</span></span>
- <span data-ttu-id="8072b-186">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8072b-186">Update</span></span>
- <span data-ttu-id="8072b-187">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="8072b-187">Managecontacts</span></span>
- <span data-ttu-id="8072b-188">Getissuers</span><span class="sxs-lookup"><span data-stu-id="8072b-188">Getissuers</span></span>
- <span data-ttu-id="8072b-189">Listissuers</span><span class="sxs-lookup"><span data-stu-id="8072b-189">Listissuers</span></span>
- <span data-ttu-id="8072b-190">Emittenti</span><span class="sxs-lookup"><span data-stu-id="8072b-190">Setissuers</span></span>
- <span data-ttu-id="8072b-191">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="8072b-191">Deleteissuers</span></span>
- <span data-ttu-id="8072b-192">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="8072b-192">Manageissuers</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-193">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="8072b-193">-PermissionsToKeys</span></span>
<span data-ttu-id="8072b-194">Specifica una matrice di autorizzazioni per le operazioni chiave da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="8072b-194">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8072b-195">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8072b-195">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8072b-196">Decrittografare</span><span class="sxs-lookup"><span data-stu-id="8072b-196">Decrypt</span></span>
- <span data-ttu-id="8072b-197">Crittografare</span><span class="sxs-lookup"><span data-stu-id="8072b-197">Encrypt</span></span>
- <span data-ttu-id="8072b-198">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="8072b-198">UnwrapKey</span></span>
- <span data-ttu-id="8072b-199">WrapKey</span><span class="sxs-lookup"><span data-stu-id="8072b-199">WrapKey</span></span>
- <span data-ttu-id="8072b-200">Verificare</span><span class="sxs-lookup"><span data-stu-id="8072b-200">Verify</span></span>
- <span data-ttu-id="8072b-201">Segno</span><span class="sxs-lookup"><span data-stu-id="8072b-201">Sign</span></span>
- <span data-ttu-id="8072b-202">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8072b-202">Get</span></span>
- <span data-ttu-id="8072b-203">Elenco</span><span class="sxs-lookup"><span data-stu-id="8072b-203">List</span></span>
- <span data-ttu-id="8072b-204">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8072b-204">Update</span></span>
- <span data-ttu-id="8072b-205">Creare</span><span class="sxs-lookup"><span data-stu-id="8072b-205">Create</span></span>
- <span data-ttu-id="8072b-206">Importazione</span><span class="sxs-lookup"><span data-stu-id="8072b-206">Import</span></span>
- <span data-ttu-id="8072b-207">Eliminare</span><span class="sxs-lookup"><span data-stu-id="8072b-207">Delete</span></span>
- <span data-ttu-id="8072b-208">Backup</span><span class="sxs-lookup"><span data-stu-id="8072b-208">Backup</span></span>
- <span data-ttu-id="8072b-209">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="8072b-209">Restore</span></span>
- <span data-ttu-id="8072b-210">Recuperare</span><span class="sxs-lookup"><span data-stu-id="8072b-210">Recover</span></span>
- <span data-ttu-id="8072b-211">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="8072b-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-212">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="8072b-212">-PermissionsToSecrets</span></span>
<span data-ttu-id="8072b-213">Specifica una matrice di autorizzazioni per le operazioni segrete da concedere a un utente o a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="8072b-213">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8072b-214">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8072b-214">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8072b-215">Ottieni</span><span class="sxs-lookup"><span data-stu-id="8072b-215">Get</span></span>
- <span data-ttu-id="8072b-216">Elenco</span><span class="sxs-lookup"><span data-stu-id="8072b-216">List</span></span>
- <span data-ttu-id="8072b-217">Impostare</span><span class="sxs-lookup"><span data-stu-id="8072b-217">Set</span></span>
- <span data-ttu-id="8072b-218">Eliminare</span><span class="sxs-lookup"><span data-stu-id="8072b-218">Delete</span></span>
- <span data-ttu-id="8072b-219">Backup</span><span class="sxs-lookup"><span data-stu-id="8072b-219">Backup</span></span>
- <span data-ttu-id="8072b-220">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="8072b-220">Restore</span></span>
- <span data-ttu-id="8072b-221">Recuperare</span><span class="sxs-lookup"><span data-stu-id="8072b-221">Recover</span></span>
- <span data-ttu-id="8072b-222">Eliminazione</span><span class="sxs-lookup"><span data-stu-id="8072b-222">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-223">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="8072b-223">-PermissionsToStorage</span></span>
<span data-ttu-id="8072b-224">Specifica le autorizzazioni dell'account di archiviazione gestita e delle operazioni di definizione SAS per concedere a un utente o a un servizio Principal.</span><span class="sxs-lookup"><span data-stu-id="8072b-224">Specifies managed storage account and sas definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-225">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8072b-225">-ResourceGroupName</span></span>
<span data-ttu-id="8072b-226">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8072b-226">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-227">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8072b-227">-ServicePrincipalName</span></span>
<span data-ttu-id="8072b-228">Specifica il nome dell'entità servizio dell'applicazione a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="8072b-228">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="8072b-229">Specifica l'ID applicazione, noto anche come ID client, registrato per l'applicazione nella directory AzureActive.</span><span class="sxs-lookup"><span data-stu-id="8072b-229">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span>
<span data-ttu-id="8072b-230">L'applicazione con il nome dell'entità servizio specificata da questo parametro deve essere registrata nella directory Azure che contiene l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8072b-230">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-231">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8072b-231">-UserPrincipalName</span></span>
<span data-ttu-id="8072b-232">Specifica il nome dell'entità utente dell'utente a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="8072b-232">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="8072b-233">Il nome dell'entità utente deve esistere nella directory associata alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8072b-233">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8072b-234">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8072b-234">-VaultName</span></span>
<span data-ttu-id="8072b-235">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8072b-235">Specifies the name of a key vault.</span></span>
<span data-ttu-id="8072b-236">Questo cmdlet modifica i criteri di accesso per il Vault chiave specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8072b-236">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="8072b-237">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8072b-237">-Confirm</span></span>
<span data-ttu-id="8072b-238">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8072b-238">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8072b-239">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8072b-239">-WhatIf</span></span>
<span data-ttu-id="8072b-240">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8072b-240">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8072b-241">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8072b-241">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8072b-242">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8072b-242">-DefaultProfile</span></span>
<span data-ttu-id="8072b-243">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8072b-243">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8072b-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8072b-244">CommonParameters</span></span>
<span data-ttu-id="8072b-245">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8072b-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8072b-246">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8072b-246">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8072b-247">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8072b-247">INPUTS</span></span>

### <span data-ttu-id="8072b-248">String, Guid, String [], switch</span><span class="sxs-lookup"><span data-stu-id="8072b-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="8072b-249">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8072b-249">OUTPUTS</span></span>

### <span data-ttu-id="8072b-250">Microsoft. Azure. Commands. Vault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="8072b-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="8072b-251">Note</span><span class="sxs-lookup"><span data-stu-id="8072b-251">NOTES</span></span>

## <span data-ttu-id="8072b-252">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8072b-252">RELATED LINKS</span></span>

[<span data-ttu-id="8072b-253">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8072b-253">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="8072b-254">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8072b-254">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)
