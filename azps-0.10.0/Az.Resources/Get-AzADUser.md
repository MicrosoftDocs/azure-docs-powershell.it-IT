---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: b5690dfc1d85483b10fc7cd08606c4555784e8e0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398734"
---
# <span data-ttu-id="03a33-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="03a33-101">Get-AzADUser</span></span>

## <span data-ttu-id="03a33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a33-102">SYNOPSIS</span></span>
<span data-ttu-id="03a33-103">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="03a33-103">Filters active directory users.</span></span>

## <span data-ttu-id="03a33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03a33-104">SYNTAX</span></span>

### <span data-ttu-id="03a33-105">EmptyParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03a33-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="03a33-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="03a33-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="03a33-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="03a33-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="03a33-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03a33-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="03a33-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="03a33-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="03a33-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="03a33-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="03a33-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03a33-111">DESCRIPTION</span></span>
<span data-ttu-id="03a33-112">Filtra gli utenti di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="03a33-112">Filters active directory users.</span></span>

## <span data-ttu-id="03a33-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03a33-113">EXAMPLES</span></span>

### <span data-ttu-id="03a33-114">Esempio 1 - Elencare tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="03a33-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="03a33-115">Elenca tutti gli utenti di Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="03a33-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="03a33-116">Esempio 2 - Elencare tutti gli utenti tramite suddivisione in pagine</span><span class="sxs-lookup"><span data-stu-id="03a33-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="03a33-117">Elenca i primi 100 utenti di Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="03a33-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="03a33-118">Esempio 3 - Ottenere un utente di Active Directory in base al nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="03a33-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="03a33-119">Ottiene l'utente Active Directory con il nome dell'entità utente " foo@domain.com ".</span><span class="sxs-lookup"><span data-stu-id="03a33-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="03a33-120">Esempio 4 - Elencare per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="03a33-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="03a33-121">Elenca tutti gli utenti di Active Directory il cui nome visualizzato inizia con "Luca".</span><span class="sxs-lookup"><span data-stu-id="03a33-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="03a33-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03a33-122">PARAMETERS</span></span>

### <span data-ttu-id="03a33-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a33-123">-DefaultProfile</span></span>
<span data-ttu-id="03a33-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="03a33-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03a33-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="03a33-125">-DisplayName</span></span>
<span data-ttu-id="03a33-126">Nome visualizzato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="03a33-126">The display name of the user.</span></span>

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

### <span data-ttu-id="03a33-127">-First</span><span class="sxs-lookup"><span data-stu-id="03a33-127">-First</span></span>
<span data-ttu-id="03a33-128">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="03a33-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="03a33-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="03a33-129">-IncludeTotalCount</span></span>
<span data-ttu-id="03a33-130">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="03a33-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="03a33-131">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="03a33-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="03a33-132">-Mail</span><span class="sxs-lookup"><span data-stu-id="03a33-132">-Mail</span></span>
<span data-ttu-id="03a33-133">Posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="03a33-133">The user mail.</span></span>

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

### <span data-ttu-id="03a33-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="03a33-134">-ObjectId</span></span>
<span data-ttu-id="03a33-135">ID oggetto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="03a33-135">Object id of the user.</span></span>

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

### <span data-ttu-id="03a33-136">-Skip</span><span class="sxs-lookup"><span data-stu-id="03a33-136">-Skip</span></span>
<span data-ttu-id="03a33-137">Ignora i primi N oggetti e quindi ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="03a33-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="03a33-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="03a33-138">-StartsWith</span></span>
<span data-ttu-id="03a33-139">Consente di trovare gli utenti che iniziano con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="03a33-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="03a33-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="03a33-140">-UserPrincipalName</span></span>
<span data-ttu-id="03a33-141">UPN dell'utente.</span><span class="sxs-lookup"><span data-stu-id="03a33-141">UPN of the user.</span></span>

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

### <span data-ttu-id="03a33-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a33-142">CommonParameters</span></span>
<span data-ttu-id="03a33-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03a33-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a33-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a33-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a33-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="03a33-145">INPUTS</span></span>

### <span data-ttu-id="03a33-146">System.String</span><span class="sxs-lookup"><span data-stu-id="03a33-146">System.String</span></span>

### <span data-ttu-id="03a33-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="03a33-147">System.Guid</span></span>

## <span data-ttu-id="03a33-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03a33-148">OUTPUTS</span></span>

### <span data-ttu-id="03a33-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="03a33-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="03a33-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="03a33-150">NOTES</span></span>

## <span data-ttu-id="03a33-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03a33-151">RELATED LINKS</span></span>

[<span data-ttu-id="03a33-152">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="03a33-152">New-AzADUser</span></span>](./New-AzADUser.md)


[<span data-ttu-id="03a33-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="03a33-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

