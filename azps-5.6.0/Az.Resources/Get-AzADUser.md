---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 6f5ae29865775368427987dcfc1844c9235db593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961693"
---
# <span data-ttu-id="02df9-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="02df9-101">Get-AzADUser</span></span>

## <span data-ttu-id="02df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02df9-102">SYNOPSIS</span></span>
<span data-ttu-id="02df9-103">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="02df9-103">Filters active directory users.</span></span>

## <span data-ttu-id="02df9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02df9-104">SYNTAX</span></span>

### <span data-ttu-id="02df9-105">EmptyParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="02df9-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="02df9-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="02df9-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="02df9-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="02df9-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="02df9-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02df9-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="02df9-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="02df9-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="02df9-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="02df9-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="02df9-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="02df9-111">DESCRIPTION</span></span>
<span data-ttu-id="02df9-112">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="02df9-112">Filters active directory users.</span></span>

## <span data-ttu-id="02df9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02df9-113">EXAMPLES</span></span>

### <span data-ttu-id="02df9-114">Esempio 1: Elencare tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="02df9-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="02df9-115">Elenca tutti gli utenti di Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="02df9-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="02df9-116">Esempio 2: Elencare tutti gli utenti tramite suddivisione in pagine</span><span class="sxs-lookup"><span data-stu-id="02df9-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="02df9-117">Elenca i primi 100 utenti di Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="02df9-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="02df9-118">Esempio 3: Ottenere un utente di Active Directory in base al nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="02df9-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="02df9-119">Ottiene l'utente Active Directory con il nome dell'entità utente " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="02df9-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="02df9-120">Esempio 4: Elencare per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="02df9-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="02df9-121">Elenca tutti gli utenti di Active Directory il cui nome visualizzato inizia con "Luca".</span><span class="sxs-lookup"><span data-stu-id="02df9-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="02df9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02df9-122">PARAMETERS</span></span>

### <span data-ttu-id="02df9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02df9-123">-DefaultProfile</span></span>
<span data-ttu-id="02df9-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="02df9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02df9-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="02df9-125">-DisplayName</span></span>
<span data-ttu-id="02df9-126">Nome visualizzato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="02df9-126">The display name of the user.</span></span>

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

### <span data-ttu-id="02df9-127">-Mail</span><span class="sxs-lookup"><span data-stu-id="02df9-127">-Mail</span></span>
<span data-ttu-id="02df9-128">Posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="02df9-128">The user mail.</span></span>

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

### <span data-ttu-id="02df9-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="02df9-129">-ObjectId</span></span>
<span data-ttu-id="02df9-130">ID oggetto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="02df9-130">Object id of the user.</span></span>

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

### <span data-ttu-id="02df9-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="02df9-131">-StartsWith</span></span>
<span data-ttu-id="02df9-132">Consente di trovare gli utenti che iniziano con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="02df9-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="02df9-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="02df9-133">-UserPrincipalName</span></span>
<span data-ttu-id="02df9-134">UPN dell'utente.</span><span class="sxs-lookup"><span data-stu-id="02df9-134">UPN of the user.</span></span>

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

### <span data-ttu-id="02df9-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="02df9-135">-IncludeTotalCount</span></span>
<span data-ttu-id="02df9-136">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="02df9-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="02df9-137">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="02df9-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="02df9-138">-Skip</span><span class="sxs-lookup"><span data-stu-id="02df9-138">-Skip</span></span>
<span data-ttu-id="02df9-139">Ignora i primi N oggetti e quindi ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="02df9-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="02df9-140">-First</span><span class="sxs-lookup"><span data-stu-id="02df9-140">-First</span></span>
<span data-ttu-id="02df9-141">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="02df9-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="02df9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02df9-142">CommonParameters</span></span>
<span data-ttu-id="02df9-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02df9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02df9-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="02df9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02df9-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="02df9-145">INPUTS</span></span>

### <span data-ttu-id="02df9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="02df9-146">System.String</span></span>

## <span data-ttu-id="02df9-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02df9-147">OUTPUTS</span></span>

### <span data-ttu-id="02df9-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="02df9-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="02df9-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="02df9-149">NOTES</span></span>

## <span data-ttu-id="02df9-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02df9-150">RELATED LINKS</span></span>

[<span data-ttu-id="02df9-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="02df9-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="02df9-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="02df9-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="02df9-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="02df9-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

