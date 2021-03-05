---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: b71a25fa7e3e7c70b363b3462294e3c071a6ce86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970334"
---
# <span data-ttu-id="483cc-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="483cc-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="483cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483cc-102">SYNOPSIS</span></span>
<span data-ttu-id="483cc-103">Rimuove le credenziali da un'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="483cc-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="483cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="483cc-104">SYNTAX</span></span>

### <span data-ttu-id="483cc-105">ObjectIdWithKeyIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="483cc-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483cc-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="483cc-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483cc-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="483cc-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483cc-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="483cc-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="483cc-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="483cc-109">DESCRIPTION</span></span>
<span data-ttu-id="483cc-110">Il Remove-AzADSpCredential cmdlet può essere usato per rimuovere una chiave delle credenziali da un'entità servizio in caso di compromissione o come parte della scadenza del rollover delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="483cc-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="483cc-111">L'entità servizio viene identificata fornendo l'ID oggetto o il nome dell'entità servizio (SPN).</span><span class="sxs-lookup"><span data-stu-id="483cc-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="483cc-112">Le credenziali da rimuovere sono identificate dal relativo ID chiave se è necessario rimuovere singole credenziali o con un parametro "Tutte" per eliminare tutte le credenziali associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="483cc-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="483cc-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="483cc-113">EXAMPLES</span></span>

### <span data-ttu-id="483cc-114">Esempio 1: Rimuovere credenziali specifiche da un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="483cc-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="483cc-115">Rimuove le credenziali con ID chiave '9044423a-60a3-45ac-9ab1-09534157ebb' dall'entità servizio con ID oggetto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="483cc-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="483cc-116">Esempio 2: Rimuovere tutte le credenziali da un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="483cc-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="483cc-117">Rimuove tutte le credenziali dall'entità servizio con il nome SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="483cc-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="483cc-118">Esempio 3: Rimuovere tutte le credenziali da un'entità servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="483cc-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="483cc-119">Ottiene l'entità servizio con ID oggetto '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' e pipe che al cmdlet di Remove-AzADSpCredential per rimuovere tutte le credenziali dall'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="483cc-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="483cc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="483cc-120">PARAMETERS</span></span>

### <span data-ttu-id="483cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483cc-121">-DefaultProfile</span></span>
<span data-ttu-id="483cc-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="483cc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="483cc-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="483cc-123">-DisplayName</span></span>
<span data-ttu-id="483cc-124">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="483cc-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483cc-125">-Force</span><span class="sxs-lookup"><span data-stu-id="483cc-125">-Force</span></span>
<span data-ttu-id="483cc-126">Passare all'eliminazione delle credenziali senza conferma.</span><span class="sxs-lookup"><span data-stu-id="483cc-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="483cc-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="483cc-127">-KeyId</span></span>
<span data-ttu-id="483cc-128">Specifica la chiave delle credenziali da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="483cc-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="483cc-129">Gli ID chiave per un'entità servizio possono essere ottenuti con il cmdlet Get-AzADSpCredential servizio.</span><span class="sxs-lookup"><span data-stu-id="483cc-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483cc-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="483cc-130">-ObjectId</span></span>
<span data-ttu-id="483cc-131">ID oggetto dell'entità servizio da cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="483cc-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483cc-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="483cc-132">-PassThru</span></span>
<span data-ttu-id="483cc-133">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="483cc-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="483cc-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="483cc-134">-ServicePrincipalName</span></span>
<span data-ttu-id="483cc-135">Nome (SPN) dell'entità servizio da cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="483cc-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483cc-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="483cc-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="483cc-137">Oggetto entità servizio da cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="483cc-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="483cc-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="483cc-138">-Confirm</span></span>
<span data-ttu-id="483cc-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="483cc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483cc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483cc-140">-WhatIf</span></span>
<span data-ttu-id="483cc-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="483cc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="483cc-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="483cc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483cc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483cc-143">CommonParameters</span></span>
<span data-ttu-id="483cc-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483cc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483cc-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="483cc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483cc-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="483cc-146">INPUTS</span></span>

### <span data-ttu-id="483cc-147">System.String</span><span class="sxs-lookup"><span data-stu-id="483cc-147">System.String</span></span>

### <span data-ttu-id="483cc-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="483cc-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="483cc-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="483cc-149">System.Guid</span></span>

## <span data-ttu-id="483cc-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="483cc-150">OUTPUTS</span></span>

### <span data-ttu-id="483cc-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="483cc-151">System.Boolean</span></span>

## <span data-ttu-id="483cc-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="483cc-152">NOTES</span></span>

## <span data-ttu-id="483cc-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="483cc-153">RELATED LINKS</span></span>

[<span data-ttu-id="483cc-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="483cc-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="483cc-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="483cc-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="483cc-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="483cc-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

