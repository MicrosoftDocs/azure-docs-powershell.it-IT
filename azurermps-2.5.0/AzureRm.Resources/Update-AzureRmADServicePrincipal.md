---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: d3e5459c81d2abbe7178652ce7b00fc35e6e3bbd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866194"
---
# <span data-ttu-id="f6919-101">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f6919-101">Update-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="f6919-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6919-102">SYNOPSIS</span></span>
<span data-ttu-id="f6919-103">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="f6919-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6919-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6919-104">SYNTAX</span></span>

### <span data-ttu-id="f6919-105">SpObjectIdWithDisplayNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6919-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzureRmADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6919-106">SpApplicationIdWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6919-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6919-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6919-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6919-108">InputObjectWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6919-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6919-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6919-109">DESCRIPTION</span></span>
<span data-ttu-id="f6919-110">Aggiorna un'entità di servizio di Azure Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="f6919-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="f6919-111">Per aggiornare le credenziali associate all'entità di servizio, usare New-AzureRmADSpCredential cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6919-111">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="f6919-112">Per aggiornare le proprietà associate all'applicazione sottostante, usare Update-AzureRmADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6919-112">To update the properties associated with the underlying application, please use Update-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="f6919-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6919-113">EXAMPLES</span></span>

### <span data-ttu-id="f6919-114">Esempio 1-aggiornare il nome visualizzato di un'entità servizio</span><span class="sxs-lookup"><span data-stu-id="f6919-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="f6919-115">Aggiorna il nome visualizzato dell'entità servizio con l'ID oggetto "784136ca-3ae2-4fdd-A388-89d793e7c780" in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="f6919-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="f6919-116">Esempio 2-aggiornare il nome visualizzato di un'entità di servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="f6919-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzureRmADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="f6919-117">Ottiene l'entità servizio con l'ID oggetto "784136ca-3ae2-4fdd-A388-89d793e7c780" e le pipe al cmdlet Update-AzureRmADServicePrincipal per aggiornare il nome visualizzato dell'entità servizio in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="f6919-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzureRmADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="f6919-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6919-118">PARAMETERS</span></span>

### <span data-ttu-id="f6919-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f6919-119">-ApplicationId</span></span>
<span data-ttu-id="f6919-120">ID applicazione dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="f6919-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="f6919-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6919-121">-DefaultProfile</span></span>
<span data-ttu-id="f6919-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6919-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6919-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f6919-123">-DisplayName</span></span>
<span data-ttu-id="f6919-124">Nome visualizzato per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="f6919-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="f6919-125">-Home page</span><span class="sxs-lookup"><span data-stu-id="f6919-125">-Homepage</span></span>
<span data-ttu-id="f6919-126">Homepage per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="f6919-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="f6919-127">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="f6919-127">-IdentifierUri</span></span>
<span data-ttu-id="f6919-128">URI (s) identificatore per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="f6919-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="f6919-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6919-129">-InputObject</span></span>
<span data-ttu-id="f6919-130">Oggetto che rappresenta l'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="f6919-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6919-131">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="f6919-131">-KeyCredential</span></span>
<span data-ttu-id="f6919-132">Le credenziali chiave per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="f6919-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6919-133">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f6919-133">-ObjectId</span></span>
<span data-ttu-id="f6919-134">ID oggetto dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="f6919-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6919-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="f6919-135">-PasswordCredential</span></span>
<span data-ttu-id="f6919-136">Credenziali password per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="f6919-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6919-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f6919-137">-ServicePrincipalName</span></span>
<span data-ttu-id="f6919-138">SPN dell'entità servizio da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="f6919-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="f6919-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f6919-139">-Confirm</span></span>
<span data-ttu-id="f6919-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6919-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6919-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6919-141">-WhatIf</span></span>
<span data-ttu-id="f6919-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6919-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6919-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6919-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6919-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6919-144">CommonParameters</span></span>
<span data-ttu-id="f6919-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6919-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6919-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6919-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6919-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6919-147">INPUTS</span></span>

### <span data-ttu-id="f6919-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="f6919-148">System.Guid</span></span>

### <span data-ttu-id="f6919-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f6919-149">System.String</span></span>

### <span data-ttu-id="f6919-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f6919-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="f6919-151">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f6919-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f6919-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6919-152">OUTPUTS</span></span>

### <span data-ttu-id="f6919-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f6919-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f6919-154">Note</span><span class="sxs-lookup"><span data-stu-id="f6919-154">NOTES</span></span>

## <span data-ttu-id="f6919-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6919-155">RELATED LINKS</span></span>
