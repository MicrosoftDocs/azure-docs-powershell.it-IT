---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 01f6b6d6ed119945af7d99bac9227c788976cbab
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398700"
---
# <span data-ttu-id="0fa63-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0fa63-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="0fa63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fa63-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa63-103">Filtra le entità servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0fa63-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="0fa63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fa63-104">SYNTAX</span></span>

### <span data-ttu-id="0fa63-105">EmptyParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0fa63-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0fa63-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa63-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0fa63-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa63-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0fa63-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa63-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0fa63-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa63-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0fa63-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa63-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0fa63-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa63-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="0fa63-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0fa63-112">DESCRIPTION</span></span>
<span data-ttu-id="0fa63-113">Filtra le entità servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0fa63-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="0fa63-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fa63-114">EXAMPLES</span></span>

### <span data-ttu-id="0fa63-115">Esempio 1 - Elencare le entità servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="0fa63-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="0fa63-116">Elenca tutte le entità servizio Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="0fa63-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="0fa63-117">Esempio 2 - Elencare le entità servizio Active Directory tramite la suddivisione in pagine</span><span class="sxs-lookup"><span data-stu-id="0fa63-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="0fa63-118">Elenca le prime 100 entità servizio Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="0fa63-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="0fa63-119">Esempio 3 - Elencare le entità servizio per SPN</span><span class="sxs-lookup"><span data-stu-id="0fa63-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="0fa63-120">Elenca le entità servizio con il nome SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span><span class="sxs-lookup"><span data-stu-id="0fa63-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="0fa63-121">Esempio 4 - Elencare le entità servizio per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="0fa63-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="0fa63-122">Elenca tutte le entità servizio Active Directory il cui nome visualizzato inizia con "Web".</span><span class="sxs-lookup"><span data-stu-id="0fa63-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="0fa63-123">Esempio 5 - Elencare le entità servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="0fa63-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="0fa63-124">Ottiene l'applicazione Active Directory con ID oggetto '39e64ec6-569b-4030-8e1c-c3c519a05d69' e la pipe al cmdlet di Get-AzADServicePrincipal per elencare tutte le entità servizio per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0fa63-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="0fa63-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fa63-125">PARAMETERS</span></span>

### <span data-ttu-id="0fa63-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0fa63-126">-ApplicationId</span></span>
<span data-ttu-id="0fa63-127">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0fa63-127">The service principal application id.</span></span>

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

### <span data-ttu-id="0fa63-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="0fa63-128">-ApplicationObject</span></span>
<span data-ttu-id="0fa63-129">Oggetto applicazione di cui è in corso il recupero dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0fa63-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="0fa63-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa63-130">-DefaultProfile</span></span>
<span data-ttu-id="0fa63-131">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0fa63-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fa63-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0fa63-132">-DisplayName</span></span>
<span data-ttu-id="0fa63-133">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0fa63-133">The service principal display name.</span></span>

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

### <span data-ttu-id="0fa63-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="0fa63-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="0fa63-135">Stringa di ricerca dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0fa63-135">The service principal search string.</span></span>

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

### <span data-ttu-id="0fa63-136">-First</span><span class="sxs-lookup"><span data-stu-id="0fa63-136">-First</span></span>
<span data-ttu-id="0fa63-137">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="0fa63-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="0fa63-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="0fa63-138">-IncludeTotalCount</span></span>
<span data-ttu-id="0fa63-139">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="0fa63-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="0fa63-140">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="0fa63-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="0fa63-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0fa63-141">-ObjectId</span></span>
<span data-ttu-id="0fa63-142">ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0fa63-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="0fa63-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0fa63-143">-ServicePrincipalName</span></span>
<span data-ttu-id="0fa63-144">Nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0fa63-144">SPN of the service.</span></span>

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

### <span data-ttu-id="0fa63-145">-Skip</span><span class="sxs-lookup"><span data-stu-id="0fa63-145">-Skip</span></span>
<span data-ttu-id="0fa63-146">Ignora i primi N oggetti e quindi ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="0fa63-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="0fa63-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa63-147">CommonParameters</span></span>
<span data-ttu-id="0fa63-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa63-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa63-149">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa63-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa63-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="0fa63-150">INPUTS</span></span>

### <span data-ttu-id="0fa63-151">System.String</span><span class="sxs-lookup"><span data-stu-id="0fa63-151">System.String</span></span>

### <span data-ttu-id="0fa63-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0fa63-152">System.Guid</span></span>

### <span data-ttu-id="0fa63-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0fa63-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="0fa63-154">Parametri: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0fa63-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="0fa63-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fa63-155">OUTPUTS</span></span>

### <span data-ttu-id="0fa63-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0fa63-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="0fa63-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="0fa63-157">NOTES</span></span>

## <span data-ttu-id="0fa63-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fa63-158">RELATED LINKS</span></span>

[<span data-ttu-id="0fa63-159">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0fa63-159">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)


[<span data-ttu-id="0fa63-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0fa63-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="0fa63-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="0fa63-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="0fa63-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0fa63-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

