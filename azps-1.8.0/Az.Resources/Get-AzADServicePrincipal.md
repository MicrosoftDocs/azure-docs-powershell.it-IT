---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 0dc49732a6e6ad614a0330c3fe24b412be898a54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677410"
---
# <span data-ttu-id="00de0-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="00de0-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="00de0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00de0-102">SYNOPSIS</span></span>
<span data-ttu-id="00de0-103">Filtra le entità del servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00de0-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="00de0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00de0-104">SYNTAX</span></span>

### <span data-ttu-id="00de0-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00de0-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00de0-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="00de0-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00de0-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00de0-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00de0-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00de0-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00de0-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00de0-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00de0-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00de0-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="00de0-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="00de0-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="00de0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00de0-112">DESCRIPTION</span></span>
<span data-ttu-id="00de0-113">Filtra le entità del servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00de0-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="00de0-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00de0-114">EXAMPLES</span></span>

### <span data-ttu-id="00de0-115">Esempio 1-elenco delle entità di servizio degli annunci pubblicitari</span><span class="sxs-lookup"><span data-stu-id="00de0-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="00de0-116">Elenca tutte le entità del servizio Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="00de0-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="00de0-117">Esempio 2-elenco delle entità di servizio degli annunci pubblicitari tramite paging</span><span class="sxs-lookup"><span data-stu-id="00de0-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="00de0-118">Elenca le prime entità di servizio degli annunci di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="00de0-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="00de0-119">Esempio 3-elenco entità servizio per SPN</span><span class="sxs-lookup"><span data-stu-id="00de0-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="00de0-120">Elenca le entità di servizio con l'SPN "36f81fc3-b00f-48CD-8218-3879f51ff39f".</span><span class="sxs-lookup"><span data-stu-id="00de0-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="00de0-121">Esempio 4-elenco delle entità di servizio tramite la stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="00de0-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="00de0-122">Elenca tutte le entità del servizio Active Directory il cui nome visualizzato inizia con "Web".</span><span class="sxs-lookup"><span data-stu-id="00de0-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="00de0-123">Esempio 5-elenco delle entità di servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="00de0-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="00de0-124">Ottiene l'applicazione di annunci con l'ID oggetto "39e64ec6-569B-4030-8e1c-c3c519a05d69" e la convoglia al cmdlet Get-AzADServicePrincipal per elencare tutte le entità di servizio per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="00de0-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="00de0-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00de0-125">PARAMETERS</span></span>

### <span data-ttu-id="00de0-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="00de0-126">-ApplicationId</span></span>
<span data-ttu-id="00de0-127">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="00de0-127">The service principal application id.</span></span>

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

### <span data-ttu-id="00de0-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="00de0-128">-ApplicationObject</span></span>
<span data-ttu-id="00de0-129">Oggetto Application di cui viene recuperato l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="00de0-129">The application object whose service principal is being retrieved.</span></span>

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

### <span data-ttu-id="00de0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00de0-130">-DefaultProfile</span></span>
<span data-ttu-id="00de0-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="00de0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00de0-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="00de0-132">-DisplayName</span></span>
<span data-ttu-id="00de0-133">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="00de0-133">The service principal display name.</span></span>

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

### <span data-ttu-id="00de0-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="00de0-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="00de0-135">Stringa di ricerca dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="00de0-135">The service principal search string.</span></span>

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

### <span data-ttu-id="00de0-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="00de0-136">-ObjectId</span></span>
<span data-ttu-id="00de0-137">ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="00de0-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="00de0-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="00de0-138">-ServicePrincipalName</span></span>
<span data-ttu-id="00de0-139">SPN del servizio.</span><span class="sxs-lookup"><span data-stu-id="00de0-139">SPN of the service.</span></span>

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

### <span data-ttu-id="00de0-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="00de0-140">-IncludeTotalCount</span></span>
<span data-ttu-id="00de0-141">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="00de0-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="00de0-142">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="00de0-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="00de0-143">-Skip</span><span class="sxs-lookup"><span data-stu-id="00de0-143">-Skip</span></span>
<span data-ttu-id="00de0-144">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="00de0-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="00de0-145">-Primo</span><span class="sxs-lookup"><span data-stu-id="00de0-145">-First</span></span>
<span data-ttu-id="00de0-146">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="00de0-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="00de0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00de0-147">CommonParameters</span></span>
<span data-ttu-id="00de0-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00de0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00de0-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00de0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00de0-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00de0-150">INPUTS</span></span>

### <span data-ttu-id="00de0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="00de0-151">System.String</span></span>

### <span data-ttu-id="00de0-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="00de0-152">System.Guid</span></span>

### <span data-ttu-id="00de0-153">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="00de0-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="00de0-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00de0-154">OUTPUTS</span></span>

### <span data-ttu-id="00de0-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="00de0-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="00de0-156">Note</span><span class="sxs-lookup"><span data-stu-id="00de0-156">NOTES</span></span>

## <span data-ttu-id="00de0-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00de0-157">RELATED LINKS</span></span>

[<span data-ttu-id="00de0-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="00de0-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="00de0-159">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="00de0-159">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="00de0-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="00de0-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="00de0-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="00de0-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="00de0-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="00de0-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

