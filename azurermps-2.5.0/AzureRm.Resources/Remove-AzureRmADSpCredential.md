---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 73fff5ff4cf612c39bacd26fed61c4e856e34128
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865734"
---
# <span data-ttu-id="7de22-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7de22-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="7de22-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7de22-102">SYNOPSIS</span></span>
<span data-ttu-id="7de22-103">Rimuove una credenziale da un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="7de22-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7de22-104">SYNTAX</span></span>

### <span data-ttu-id="7de22-105">ObjectIdWithKeyIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7de22-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de22-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7de22-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de22-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7de22-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de22-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7de22-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de22-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7de22-109">DESCRIPTION</span></span>
<span data-ttu-id="7de22-110">Il cmdlet Remove-AzureRmADSpCredential può essere usato per rimuovere una chiave di credenziale da un'entità di servizio nel caso di un compromesso o come parte della scadenza del rollover della chiave di credenziale.</span><span class="sxs-lookup"><span data-stu-id="7de22-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="7de22-111">L'entità servizio viene identificata fornendo l'ID oggetto o il nome dell'entità servizio (SPN).</span><span class="sxs-lookup"><span data-stu-id="7de22-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="7de22-112">Le credenziali da rimuovere vengono identificate dall'ID chiave se una singola credenziale deve essere rimossa o con un'opzione ' tutti ' per eliminare tutte le credenziali associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7de22-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="7de22-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7de22-113">EXAMPLES</span></span>

### <span data-ttu-id="7de22-114">Esempio 1-rimuovere una specifica credenziale da un'entità di servizio</span><span class="sxs-lookup"><span data-stu-id="7de22-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="7de22-115">Rimuove le credenziali con l'ID chiave ' 9044423a-60A3-45AC-9ab1-09534157ebb ' dall'entità servizio con l'ID oggetto ' 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span><span class="sxs-lookup"><span data-stu-id="7de22-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="7de22-116">Esempio 2-Rimuovere tutte le credenziali da un'entità di servizio</span><span class="sxs-lookup"><span data-stu-id="7de22-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="7de22-117">Rimuove tutte le credenziali dall'entità servizio con l'SPN " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="7de22-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="7de22-118">Esempio 3-rimuovere tutte le credenziali da un'entità di servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="7de22-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADSpCredential
```

<span data-ttu-id="7de22-119">Ottiene l'entità servizio con l'ID oggetto "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" e le pipe al cmdlet Remove-AzureRmADSpCredential per rimuovere tutte le credenziali dall'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="7de22-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="7de22-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7de22-120">PARAMETERS</span></span>

### <span data-ttu-id="7de22-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de22-121">-DefaultProfile</span></span>
<span data-ttu-id="7de22-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7de22-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7de22-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7de22-123">-DisplayName</span></span>
<span data-ttu-id="7de22-124">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7de22-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="7de22-125">-Force</span><span class="sxs-lookup"><span data-stu-id="7de22-125">-Force</span></span>
<span data-ttu-id="7de22-126">Passare a eliminare le credenziali senza conferma.</span><span class="sxs-lookup"><span data-stu-id="7de22-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="7de22-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7de22-127">-KeyId</span></span>
<span data-ttu-id="7de22-128">Specifica la chiave delle credenziali da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7de22-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="7de22-129">Gli ID chiave per un'entità di servizio possono essere ottenuti usando il cmdlet Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="7de22-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="7de22-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7de22-130">-ObjectId</span></span>
<span data-ttu-id="7de22-131">ID oggetto dell'entità servizio da cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7de22-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de22-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7de22-132">-PassThru</span></span>
<span data-ttu-id="7de22-133">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="7de22-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7de22-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7de22-134">-ServicePrincipalName</span></span>
<span data-ttu-id="7de22-135">Nome (SPN) dell'entità servizio per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7de22-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="7de22-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="7de22-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="7de22-137">Oggetto Principal del servizio per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="7de22-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7de22-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7de22-138">-Confirm</span></span>
<span data-ttu-id="7de22-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7de22-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de22-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de22-140">-WhatIf</span></span>
<span data-ttu-id="7de22-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7de22-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de22-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7de22-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de22-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de22-143">CommonParameters</span></span>
<span data-ttu-id="7de22-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de22-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de22-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de22-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de22-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7de22-146">INPUTS</span></span>

### <span data-ttu-id="7de22-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7de22-147">System.Guid</span></span>

### <span data-ttu-id="7de22-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7de22-148">System.String</span></span>

### <span data-ttu-id="7de22-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7de22-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="7de22-150">Parametri: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7de22-150">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="7de22-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7de22-151">OUTPUTS</span></span>

### <span data-ttu-id="7de22-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7de22-152">System.Boolean</span></span>

## <span data-ttu-id="7de22-153">Note</span><span class="sxs-lookup"><span data-stu-id="7de22-153">NOTES</span></span>

## <span data-ttu-id="7de22-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7de22-154">RELATED LINKS</span></span>

[<span data-ttu-id="7de22-155">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7de22-155">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="7de22-156">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7de22-156">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="7de22-157">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7de22-157">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

