---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 05bd5f7997c83c2be6b50faf0e6d88ee7413a773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325525"
---
# <span data-ttu-id="49592-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49592-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="49592-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49592-102">SYNOPSIS</span></span>
<span data-ttu-id="49592-103">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="49592-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="49592-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49592-104">SYNTAX</span></span>

### <span data-ttu-id="49592-105">SpObjectIdWithDisplayNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49592-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49592-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49592-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49592-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49592-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49592-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49592-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49592-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49592-109">DESCRIPTION</span></span>
<span data-ttu-id="49592-110">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="49592-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="49592-111">Per aggiornare le credenziali associate all'entità di servizio, usare New-AzADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49592-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="49592-112">Per aggiornare le proprietà associate all'applicazione sottostante, usare Update-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49592-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="49592-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49592-113">EXAMPLES</span></span>

### <span data-ttu-id="49592-114">Esempio 1: aggiornare il nome visualizzato di un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="49592-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="49592-115">Aggiorna il nome visualizzato dell'entità servizio con l'ID oggetto "784136ca-3ae2-4fdd-A388-89d793e7c780" in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="49592-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="49592-116">Esempio 2: aggiornare il nome visualizzato di un'entità di servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="49592-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="49592-117">Ottiene l'entità servizio con l'ID oggetto "784136ca-3ae2-4fdd-A388-89d793e7c780" e le pipe al cmdlet Update-AzADServicePrincipal per aggiornare il nome visualizzato dell'entità servizio in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="49592-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="49592-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="49592-118">Example 3</span></span>

<span data-ttu-id="49592-119">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="49592-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="49592-120">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="49592-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="49592-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49592-121">PARAMETERS</span></span>

### <span data-ttu-id="49592-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="49592-122">-ApplicationId</span></span>
<span data-ttu-id="49592-123">ID applicazione dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="49592-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="49592-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49592-124">-DefaultProfile</span></span>
<span data-ttu-id="49592-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49592-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49592-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49592-126">-DisplayName</span></span>
<span data-ttu-id="49592-127">Nome visualizzato per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="49592-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="49592-128">-Home page</span><span class="sxs-lookup"><span data-stu-id="49592-128">-Homepage</span></span>
<span data-ttu-id="49592-129">Homepage per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="49592-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="49592-130">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="49592-130">-IdentifierUri</span></span>
<span data-ttu-id="49592-131">URI (s) identificatore per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="49592-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="49592-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49592-132">-InputObject</span></span>
<span data-ttu-id="49592-133">Oggetto che rappresenta l'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="49592-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="49592-134">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="49592-134">-KeyCredential</span></span>
<span data-ttu-id="49592-135">Le credenziali chiave per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="49592-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="49592-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="49592-136">-ObjectId</span></span>
<span data-ttu-id="49592-137">ID oggetto dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="49592-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="49592-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="49592-138">-PasswordCredential</span></span>
<span data-ttu-id="49592-139">Credenziali password per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="49592-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="49592-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="49592-140">-ServicePrincipalName</span></span>
<span data-ttu-id="49592-141">SPN dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="49592-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="49592-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49592-142">-Confirm</span></span>
<span data-ttu-id="49592-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49592-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49592-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49592-144">-WhatIf</span></span>
<span data-ttu-id="49592-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49592-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49592-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49592-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49592-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49592-147">CommonParameters</span></span>
<span data-ttu-id="49592-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49592-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49592-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49592-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49592-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49592-150">INPUTS</span></span>

### <span data-ttu-id="49592-151">System. String</span><span class="sxs-lookup"><span data-stu-id="49592-151">System.String</span></span>

### <span data-ttu-id="49592-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="49592-152">System.Guid</span></span>

### <span data-ttu-id="49592-153">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49592-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="49592-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49592-154">OUTPUTS</span></span>

### <span data-ttu-id="49592-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49592-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="49592-156">Note</span><span class="sxs-lookup"><span data-stu-id="49592-156">NOTES</span></span>

## <span data-ttu-id="49592-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49592-157">RELATED LINKS</span></span>