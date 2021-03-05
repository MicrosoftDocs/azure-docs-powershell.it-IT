---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 659c2a026099eaa8764030b86a40d9ca6d4d2333
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961709"
---
# <span data-ttu-id="a891b-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a891b-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="a891b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a891b-102">SYNOPSIS</span></span>
<span data-ttu-id="a891b-103">Filtra le entità servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a891b-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="a891b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a891b-104">SYNTAX</span></span>

### <span data-ttu-id="a891b-105">EmptyParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a891b-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a891b-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a891b-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a891b-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a891b-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a891b-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a891b-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a891b-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a891b-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a891b-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a891b-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a891b-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a891b-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="a891b-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a891b-112">DESCRIPTION</span></span>
<span data-ttu-id="a891b-113">Filtra le entità servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a891b-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="a891b-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a891b-114">EXAMPLES</span></span>

### <span data-ttu-id="a891b-115">Esempio 1: Elencare le entità servizio Active Directory</span><span class="sxs-lookup"><span data-stu-id="a891b-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="a891b-116">Elenca tutte le entità servizio Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="a891b-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="a891b-117">Esempio 2: Elencare le entità servizio Active Directory tramite la suddivisione in pagine</span><span class="sxs-lookup"><span data-stu-id="a891b-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="a891b-118">Elenca le prime 100 entità servizio Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="a891b-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="a891b-119">Esempio 3: Elencare le entità servizio per SPN</span><span class="sxs-lookup"><span data-stu-id="a891b-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="a891b-120">Elenca le entità servizio con il nome SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span><span class="sxs-lookup"><span data-stu-id="a891b-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="a891b-121">Esempio 4: Elencare le entità servizio per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="a891b-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="a891b-122">Elenca tutte le entità servizio Active Directory il cui nome visualizzato inizia con "Web".</span><span class="sxs-lookup"><span data-stu-id="a891b-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="a891b-123">Esempio 5: Elencare le entità servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="a891b-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="a891b-124">Ottiene l'applicazione Active Directory con ID oggetto '39e64ec6-569b-4030-8e1c-c3c519a05d69' e la pipe al cmdlet di Get-AzADServicePrincipal per elencare tutte le entità servizio per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a891b-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="a891b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a891b-125">PARAMETERS</span></span>

### <span data-ttu-id="a891b-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a891b-126">-ApplicationId</span></span>
<span data-ttu-id="a891b-127">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a891b-127">The service principal application id.</span></span>

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

### <span data-ttu-id="a891b-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="a891b-128">-ApplicationObject</span></span>
<span data-ttu-id="a891b-129">Oggetto applicazione di cui è in corso il recupero dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a891b-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a891b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a891b-130">-DefaultProfile</span></span>
<span data-ttu-id="a891b-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a891b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a891b-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a891b-132">-DisplayName</span></span>
<span data-ttu-id="a891b-133">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a891b-133">The service principal display name.</span></span>

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

### <span data-ttu-id="a891b-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="a891b-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="a891b-135">Stringa di ricerca dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a891b-135">The service principal search string.</span></span>

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

### <span data-ttu-id="a891b-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a891b-136">-ObjectId</span></span>
<span data-ttu-id="a891b-137">ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a891b-137">Object id of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a891b-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a891b-138">-ServicePrincipalName</span></span>
<span data-ttu-id="a891b-139">Nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="a891b-139">SPN of the service.</span></span>

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

### <span data-ttu-id="a891b-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="a891b-140">-IncludeTotalCount</span></span>
<span data-ttu-id="a891b-141">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="a891b-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="a891b-142">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="a891b-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="a891b-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="a891b-143">-Skip</span></span>
<span data-ttu-id="a891b-144">Ignora i primi N oggetti e quindi ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="a891b-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="a891b-145">-First</span><span class="sxs-lookup"><span data-stu-id="a891b-145">-First</span></span>
<span data-ttu-id="a891b-146">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="a891b-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="a891b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a891b-147">CommonParameters</span></span>
<span data-ttu-id="a891b-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a891b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a891b-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a891b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a891b-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="a891b-150">INPUTS</span></span>

### <span data-ttu-id="a891b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a891b-151">System.String</span></span>

### <span data-ttu-id="a891b-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a891b-152">System.Guid</span></span>

### <span data-ttu-id="a891b-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a891b-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a891b-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a891b-154">OUTPUTS</span></span>

### <span data-ttu-id="a891b-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a891b-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="a891b-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="a891b-156">NOTES</span></span>

## <span data-ttu-id="a891b-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a891b-157">RELATED LINKS</span></span>

[<span data-ttu-id="a891b-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a891b-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="a891b-159">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a891b-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="a891b-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a891b-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="a891b-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a891b-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="a891b-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a891b-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

