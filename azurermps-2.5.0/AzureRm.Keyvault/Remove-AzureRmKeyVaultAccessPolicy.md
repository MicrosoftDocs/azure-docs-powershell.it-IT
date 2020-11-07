---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 421a2becff4c32f4c29990f32cbf1a4c6e9a3e84
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865787"
---
# <span data-ttu-id="a29d1-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a29d1-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="a29d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a29d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a29d1-103">Rimuove tutte le autorizzazioni per un utente o un'applicazione da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a29d1-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a29d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a29d1-104">SYNTAX</span></span>

### <span data-ttu-id="a29d1-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a29d1-105">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a29d1-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a29d1-106">ByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a29d1-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="a29d1-107">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a29d1-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="a29d1-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a29d1-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="a29d1-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a29d1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a29d1-110">DESCRIPTION</span></span>
<span data-ttu-id="a29d1-111">Il cmdlet **Remove-AzureRmKeyVaultAccessPolicy** consente di rimuovere tutte le autorizzazioni per un utente o un'applicazione o per tutti gli utenti e le applicazioni da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a29d1-111">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="a29d1-112">Anche se si rimuovono tutte le autorizzazioni, il proprietario dell'abbonamento Azure che contiene il Vault chiave può aggiungere le autorizzazioni per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a29d1-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="a29d1-113">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, devi farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a29d1-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="a29d1-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a29d1-114">EXAMPLES</span></span>

### <span data-ttu-id="a29d1-115">Esempio 1: rimuovere le autorizzazioni per un utente</span><span class="sxs-lookup"><span data-stu-id="a29d1-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="a29d1-116">Questo comando rimuove tutte le autorizzazioni che un utente PattiFuller@contoso.com ha sul Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="a29d1-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="a29d1-117">Esempio 2: rimuovere le autorizzazioni per un'applicazione</span><span class="sxs-lookup"><span data-stu-id="a29d1-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="a29d1-118">Questo comando consente di rimuovere tutte le autorizzazioni di un'applicazione nel Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="a29d1-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="a29d1-119">Questo esempio identifica l'applicazione usando il nome dell'entità servizio registrata in Azure Active Directory http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="a29d1-119">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="a29d1-120">Esempio 3: rimuovere le autorizzazioni per un'applicazione usando l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="a29d1-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="a29d1-121">Questo comando consente di rimuovere tutte le autorizzazioni di un'applicazione nel Vault chiave denominato Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="a29d1-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="a29d1-122">Questo esempio identifica l'applicazione dall'ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a29d1-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="a29d1-123">Esempio 4: rimuovere le autorizzazioni per il provider di risorse Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="a29d1-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="a29d1-124">Questo comando rimuove l'autorizzazione per il provider di risorse Microsoft. COMPUTE per ottenere i segreti da Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="a29d1-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="a29d1-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a29d1-125">PARAMETERS</span></span>

### <span data-ttu-id="a29d1-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a29d1-126">-ApplicationId</span></span>
<span data-ttu-id="a29d1-127">Per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a29d1-127">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29d1-128">-DefaultProfile</span></span>
<span data-ttu-id="a29d1-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a29d1-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-130">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a29d1-130">-EmailAddress</span></span>
<span data-ttu-id="a29d1-131">Specifica l'indirizzo di posta elettronica dell'utente di cui si vuole rimuovere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="a29d1-131">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-132">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="a29d1-132">-EnabledForDeployment</span></span>
<span data-ttu-id="a29d1-133">Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a29d1-133">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-134">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a29d1-134">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="a29d1-135">Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="a29d1-135">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-136">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="a29d1-136">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="a29d1-137">Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="a29d1-137">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-138">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a29d1-138">-ObjectId</span></span>
<span data-ttu-id="a29d1-139">Specifica l'ID oggetto dell'entità di servizio o dell'utente in Azure Active Directory per cui rimuovere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="a29d1-139">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a29d1-140">-PassThru</span></span>
<span data-ttu-id="a29d1-141">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a29d1-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a29d1-142">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a29d1-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a29d1-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a29d1-143">-ResourceGroupName</span></span>
<span data-ttu-id="a29d1-144">Specifica il nome del gruppo di risorse associato alla volta chiave in cui vengono modificati i criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="a29d1-144">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="a29d1-145">Se non viene specificato, questo cmdlet cerca il Vault chiave nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a29d1-145">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-146">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a29d1-146">-ServicePrincipalName</span></span>
<span data-ttu-id="a29d1-147">Specifica il nome dell'entità servizio dell'applicazione di cui si vogliono rimuovere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="a29d1-147">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="a29d1-148">Specificare l'ID applicazione, noto anche come ID client, registrato per l'applicazione in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a29d1-148">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-149">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a29d1-149">-UserPrincipalName</span></span>
<span data-ttu-id="a29d1-150">Specifica il nome dell'entità utente dell'utente di cui si vuole rimuovere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="a29d1-150">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-151">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="a29d1-151">-VaultName</span></span>
<span data-ttu-id="a29d1-152">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a29d1-152">Specifies the name of the key vault.</span></span>
<span data-ttu-id="a29d1-153">Questo cmdlet consente di rimuovere le autorizzazioni per il Vault chiave specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a29d1-153">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="a29d1-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a29d1-154">-Confirm</span></span>
<span data-ttu-id="a29d1-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a29d1-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a29d1-156">-WhatIf</span></span>
<span data-ttu-id="a29d1-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a29d1-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a29d1-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a29d1-158">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29d1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29d1-159">CommonParameters</span></span>
<span data-ttu-id="a29d1-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a29d1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29d1-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a29d1-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29d1-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a29d1-162">INPUTS</span></span>

## <span data-ttu-id="a29d1-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a29d1-163">OUTPUTS</span></span>

### <span data-ttu-id="a29d1-164">Microsoft. Azure. Commands. Vault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="a29d1-164">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="a29d1-165">Note</span><span class="sxs-lookup"><span data-stu-id="a29d1-165">NOTES</span></span>

## <span data-ttu-id="a29d1-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a29d1-166">RELATED LINKS</span></span>

[<span data-ttu-id="a29d1-167">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a29d1-167">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

