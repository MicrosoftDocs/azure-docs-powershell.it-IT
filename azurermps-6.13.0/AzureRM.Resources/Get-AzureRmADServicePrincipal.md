---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 983d5049d0ac58671b3d0766b6b4bcf3f05d4d76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514872"
---
# <span data-ttu-id="3a4bc-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3a4bc-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="3a4bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4bc-103">Filtra le entità del servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a4bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a4bc-104">SYNTAX</span></span>

### <span data-ttu-id="3a4bc-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a4bc-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3a4bc-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a4bc-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3a4bc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a4bc-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3a4bc-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a4bc-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3a4bc-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a4bc-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3a4bc-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a4bc-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="3a4bc-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a4bc-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="3a4bc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a4bc-112">DESCRIPTION</span></span>
<span data-ttu-id="3a4bc-113">Filtra le entità del servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="3a4bc-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a4bc-114">EXAMPLES</span></span>

### <span data-ttu-id="3a4bc-115">Esempio 1-elenco delle entità di servizio degli annunci pubblicitari</span><span class="sxs-lookup"><span data-stu-id="3a4bc-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="3a4bc-116">Elenca tutte le entità del servizio Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="3a4bc-117">Esempio 2-elenco delle entità di servizio degli annunci pubblicitari tramite paging</span><span class="sxs-lookup"><span data-stu-id="3a4bc-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="3a4bc-118">Elenca le prime entità di servizio degli annunci di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="3a4bc-119">Esempio 3-elenco entità servizio per SPN</span><span class="sxs-lookup"><span data-stu-id="3a4bc-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="3a4bc-120">Elenca le entità di servizio con l'SPN "36f81fc3-b00f-48CD-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="3a4bc-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="3a4bc-121">Esempio 4-elenco delle entità di servizio tramite la stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="3a4bc-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="3a4bc-122">Elenca tutte le entità del servizio Active Directory il cui nome visualizzato inizia con "Web".</span><span class="sxs-lookup"><span data-stu-id="3a4bc-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="3a4bc-123">Esempio 5-elenco delle entità di servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="3a4bc-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="3a4bc-124">Ottiene l'applicazione di annunci con l'ID oggetto "39e64ec6-569B-4030-8e1c-c3c519a05d69" e la convoglia al cmdlet Get-AzureRmADServicePrincipal per elencare tutte le entità di servizio per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="3a4bc-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a4bc-125">PARAMETERS</span></span>

### <span data-ttu-id="3a4bc-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3a4bc-126">-ApplicationId</span></span>
<span data-ttu-id="3a4bc-127">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-127">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4bc-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="3a4bc-128">-ApplicationObject</span></span>
<span data-ttu-id="3a4bc-129">Oggetto Application di cui viene recuperato l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4bc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4bc-130">-DefaultProfile</span></span>
<span data-ttu-id="3a4bc-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3a4bc-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a4bc-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3a4bc-132">-DisplayName</span></span>
<span data-ttu-id="3a4bc-133">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-133">The service principal display name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4bc-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="3a4bc-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="3a4bc-135">Stringa di ricerca dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-135">The service principal search string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4bc-136">-Primo</span><span class="sxs-lookup"><span data-stu-id="3a4bc-136">-First</span></span>
<span data-ttu-id="3a4bc-137">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-137">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a4bc-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="3a4bc-138">-IncludeTotalCount</span></span>
<span data-ttu-id="3a4bc-139">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="3a4bc-140">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="3a4bc-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3a4bc-141">-ObjectId</span></span>
<span data-ttu-id="3a4bc-142">ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-142">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4bc-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3a4bc-143">-ServicePrincipalName</span></span>
<span data-ttu-id="3a4bc-144">SPN del servizio.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-144">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a4bc-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="3a4bc-145">-Skip</span></span>
<span data-ttu-id="3a4bc-146">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-146">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a4bc-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4bc-147">CommonParameters</span></span>
<span data-ttu-id="3a4bc-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a4bc-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4bc-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a4bc-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4bc-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a4bc-150">INPUTS</span></span>

### <span data-ttu-id="3a4bc-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3a4bc-151">System.String</span></span>

### <span data-ttu-id="3a4bc-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="3a4bc-152">System.Guid</span></span>

### <span data-ttu-id="3a4bc-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3a4bc-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="3a4bc-154">Parametri: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3a4bc-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="3a4bc-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a4bc-155">OUTPUTS</span></span>

### <span data-ttu-id="3a4bc-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3a4bc-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="3a4bc-157">Note</span><span class="sxs-lookup"><span data-stu-id="3a4bc-157">NOTES</span></span>

## <span data-ttu-id="3a4bc-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a4bc-158">RELATED LINKS</span></span>

[<span data-ttu-id="3a4bc-159">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3a4bc-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3a4bc-160">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3a4bc-160">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3a4bc-161">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3a4bc-161">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="3a4bc-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="3a4bc-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="3a4bc-163">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="3a4bc-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)
