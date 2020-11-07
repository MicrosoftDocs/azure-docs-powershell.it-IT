---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e4fafb6c1ddc4dda05b6536501f713d04c312172
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677250"
---
# <span data-ttu-id="40d77-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="40d77-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="40d77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40d77-102">SYNOPSIS</span></span>
<span data-ttu-id="40d77-103">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="40d77-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="40d77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40d77-104">SYNTAX</span></span>

### <span data-ttu-id="40d77-105">SpObjectIdWithDisplayNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40d77-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d77-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d77-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d77-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d77-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40d77-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="40d77-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40d77-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40d77-109">DESCRIPTION</span></span>
<span data-ttu-id="40d77-110">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="40d77-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="40d77-111">Per aggiornare le credenziali associate all'entità di servizio, usare New-AzADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d77-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="40d77-112">Per aggiornare le proprietà associate all'applicazione sottostante, usare Update-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d77-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="40d77-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40d77-113">EXAMPLES</span></span>

### <span data-ttu-id="40d77-114">Esempio 1-aggiornare il nome visualizzato di un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="40d77-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="40d77-115">Aggiorna il nome visualizzato dell'entità servizio con l'ID oggetto "784136ca-3ae2-4fdd-A388-89d793e7c780" in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="40d77-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="40d77-116">Esempio 2-aggiornare il nome visualizzato di un'entità di servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="40d77-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="40d77-117">Ottiene l'entità servizio con l'ID oggetto "784136ca-3ae2-4fdd-A388-89d793e7c780" e le pipe al cmdlet Update-AzADServicePrincipal per aggiornare il nome visualizzato dell'entità servizio in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="40d77-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="40d77-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40d77-118">PARAMETERS</span></span>

### <span data-ttu-id="40d77-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="40d77-119">-ApplicationId</span></span>
<span data-ttu-id="40d77-120">ID applicazione dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="40d77-120">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d77-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d77-121">-DefaultProfile</span></span>
<span data-ttu-id="40d77-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40d77-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40d77-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="40d77-123">-DisplayName</span></span>
<span data-ttu-id="40d77-124">Nome visualizzato per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="40d77-124">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d77-125">-Home page</span><span class="sxs-lookup"><span data-stu-id="40d77-125">-Homepage</span></span>
<span data-ttu-id="40d77-126">Homepage per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="40d77-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="40d77-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="40d77-127">-IdentifierUri</span></span>
<span data-ttu-id="40d77-128">URI (s) identificatore per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="40d77-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="40d77-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40d77-129">-InputObject</span></span>
<span data-ttu-id="40d77-130">Oggetto che rappresenta l'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="40d77-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40d77-131">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="40d77-131">-KeyCredential</span></span>
<span data-ttu-id="40d77-132">Le credenziali chiave per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="40d77-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d77-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="40d77-133">-ObjectId</span></span>
<span data-ttu-id="40d77-134">ID oggetto dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="40d77-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d77-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="40d77-135">-PasswordCredential</span></span>
<span data-ttu-id="40d77-136">Credenziali password per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="40d77-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d77-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="40d77-137">-ServicePrincipalName</span></span>
<span data-ttu-id="40d77-138">SPN dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="40d77-138">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40d77-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40d77-139">-Confirm</span></span>
<span data-ttu-id="40d77-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40d77-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40d77-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40d77-141">-WhatIf</span></span>
<span data-ttu-id="40d77-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40d77-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40d77-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40d77-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40d77-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d77-144">CommonParameters</span></span>
<span data-ttu-id="40d77-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40d77-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d77-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d77-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d77-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40d77-147">INPUTS</span></span>

### <span data-ttu-id="40d77-148">System. String</span><span class="sxs-lookup"><span data-stu-id="40d77-148">System.String</span></span>

### <span data-ttu-id="40d77-149">System. Guid</span><span class="sxs-lookup"><span data-stu-id="40d77-149">System.Guid</span></span>

### <span data-ttu-id="40d77-150">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="40d77-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="40d77-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40d77-151">OUTPUTS</span></span>

### <span data-ttu-id="40d77-152">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="40d77-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="40d77-153">Note</span><span class="sxs-lookup"><span data-stu-id="40d77-153">NOTES</span></span>

## <span data-ttu-id="40d77-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40d77-154">RELATED LINKS</span></span>