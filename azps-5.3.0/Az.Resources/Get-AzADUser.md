---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 884d5086c8966da8622d48e85f5f4b3009fcc94f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474303"
---
# <span data-ttu-id="d9cdc-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d9cdc-101">Get-AzADUser</span></span>

## <span data-ttu-id="d9cdc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cdc-103">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-103">Filters active directory users.</span></span>

## <span data-ttu-id="d9cdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9cdc-104">SYNTAX</span></span>

### <span data-ttu-id="d9cdc-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9cdc-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d9cdc-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cdc-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d9cdc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cdc-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d9cdc-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cdc-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d9cdc-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cdc-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="d9cdc-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cdc-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="d9cdc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9cdc-111">DESCRIPTION</span></span>
<span data-ttu-id="d9cdc-112">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-112">Filters active directory users.</span></span>

## <span data-ttu-id="d9cdc-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9cdc-113">EXAMPLES</span></span>

### <span data-ttu-id="d9cdc-114">Esempio 1: elenca tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="d9cdc-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="d9cdc-115">Elenca tutti gli utenti degli annunci in un tenant.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="d9cdc-116">Esempio 2: elenca tutti gli utenti che usano il paging</span><span class="sxs-lookup"><span data-stu-id="d9cdc-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="d9cdc-117">Elenca i primi utenti di annunci di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="d9cdc-118">Esempio 3: ottenere l'utente degli annunci per nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="d9cdc-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="d9cdc-119">Ottiene l'utente dell'annuncio con il nome dell'entità utente " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="d9cdc-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="d9cdc-120">Esempio 4: elenco per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="d9cdc-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="d9cdc-121">Elenca tutti gli utenti di Active Directory il cui nome visualizzato inizia con "Joe".</span><span class="sxs-lookup"><span data-stu-id="d9cdc-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="d9cdc-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9cdc-122">PARAMETERS</span></span>

### <span data-ttu-id="d9cdc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cdc-123">-DefaultProfile</span></span>
<span data-ttu-id="d9cdc-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d9cdc-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9cdc-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d9cdc-125">-DisplayName</span></span>
<span data-ttu-id="d9cdc-126">Nome visualizzato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-126">The display name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9cdc-127">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="d9cdc-127">-Mail</span></span>
<span data-ttu-id="d9cdc-128">Messaggio di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-128">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9cdc-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d9cdc-129">-ObjectId</span></span>
<span data-ttu-id="d9cdc-130">ID oggetto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-130">Object id of the user.</span></span>

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

### <span data-ttu-id="d9cdc-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="d9cdc-131">-StartsWith</span></span>
<span data-ttu-id="d9cdc-132">Usato per trovare gli utenti che iniziano con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="d9cdc-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d9cdc-133">-UserPrincipalName</span></span>
<span data-ttu-id="d9cdc-134">UPN dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-134">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9cdc-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="d9cdc-135">-IncludeTotalCount</span></span>
<span data-ttu-id="d9cdc-136">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="d9cdc-137">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="d9cdc-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="d9cdc-138">-Skip</span></span>
<span data-ttu-id="d9cdc-139">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="d9cdc-140">-Primo</span><span class="sxs-lookup"><span data-stu-id="d9cdc-140">-First</span></span>
<span data-ttu-id="d9cdc-141">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="d9cdc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cdc-142">CommonParameters</span></span>
<span data-ttu-id="d9cdc-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9cdc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cdc-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9cdc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cdc-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9cdc-145">INPUTS</span></span>

### <span data-ttu-id="d9cdc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d9cdc-146">System.String</span></span>

## <span data-ttu-id="d9cdc-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9cdc-147">OUTPUTS</span></span>

### <span data-ttu-id="d9cdc-148">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="d9cdc-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="d9cdc-149">Note</span><span class="sxs-lookup"><span data-stu-id="d9cdc-149">NOTES</span></span>

## <span data-ttu-id="d9cdc-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9cdc-150">RELATED LINKS</span></span>

[<span data-ttu-id="d9cdc-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d9cdc-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="d9cdc-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d9cdc-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="d9cdc-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="d9cdc-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

