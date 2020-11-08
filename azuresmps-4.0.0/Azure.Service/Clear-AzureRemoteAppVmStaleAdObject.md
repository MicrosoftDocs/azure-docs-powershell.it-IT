---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023661"
---
# <span data-ttu-id="a9850-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="a9850-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="a9850-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9850-102">SYNOPSIS</span></span>
<span data-ttu-id="a9850-103">Rimuove gli oggetti in Azure Active Directory associati alle macchine virtuali di Azure RemoteApp che non esistono più.</span><span class="sxs-lookup"><span data-stu-id="a9850-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="a9850-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9850-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9850-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9850-105">DESCRIPTION</span></span>
<span data-ttu-id="a9850-106">Il cmdlet **Clear-AzureRemoteAppVmStaleAdObject** rimuove gli oggetti in Azure Active Directory associati alle macchine virtuali di Azure RemoteApp che non esistono più.</span><span class="sxs-lookup"><span data-stu-id="a9850-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="a9850-107">È necessario utilizzare le credenziali con diritti per rimuovere gli oggetti di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a9850-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="a9850-108">Se specifichi il parametro comune *verbose* , questo cmdlet Visualizza il nome di ogni oggetto che viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="a9850-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="a9850-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9850-109">EXAMPLES</span></span>

### <span data-ttu-id="a9850-110">Esempio 1: cancellare gli oggetti obsoleti per una raccolta</span><span class="sxs-lookup"><span data-stu-id="a9850-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="a9850-111">Il primo comando richiede un nome utente e una password utilizzando **Get-Credential**.</span><span class="sxs-lookup"><span data-stu-id="a9850-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="a9850-112">Il comando Archivia i risultati nella variabile $AdminCredentials.</span><span class="sxs-lookup"><span data-stu-id="a9850-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="a9850-113">Il secondo comando Cancella gli oggetti non aggiornati per la raccolta denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="a9850-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="a9850-114">Il comando usa le credenziali archiviate in $AdminCredentials variabile.</span><span class="sxs-lookup"><span data-stu-id="a9850-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="a9850-115">Affinché il comando abbia esito positivo, tali credenziali devono avere diritti appropriati.</span><span class="sxs-lookup"><span data-stu-id="a9850-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="a9850-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9850-116">PARAMETERS</span></span>

### <span data-ttu-id="a9850-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="a9850-117">-CollectionName</span></span>
<span data-ttu-id="a9850-118">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="a9850-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9850-119">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="a9850-119">-Credential</span></span>
<span data-ttu-id="a9850-120">Specifica una credenziale con diritti per eseguire questa azione.</span><span class="sxs-lookup"><span data-stu-id="a9850-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="a9850-121">Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="a9850-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="a9850-122">Se non specifichi questo parametro, questo cmdlet usa le credenziali utente correnti.</span><span class="sxs-lookup"><span data-stu-id="a9850-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9850-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="a9850-123">-Profile</span></span>
<span data-ttu-id="a9850-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9850-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9850-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a9850-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9850-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9850-126">-Confirm</span></span>
<span data-ttu-id="a9850-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9850-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9850-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9850-128">-WhatIf</span></span>
<span data-ttu-id="a9850-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9850-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9850-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9850-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9850-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9850-131">CommonParameters</span></span>
<span data-ttu-id="a9850-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9850-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9850-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9850-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9850-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9850-134">INPUTS</span></span>

## <span data-ttu-id="a9850-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9850-135">OUTPUTS</span></span>

## <span data-ttu-id="a9850-136">Note</span><span class="sxs-lookup"><span data-stu-id="a9850-136">NOTES</span></span>

## <span data-ttu-id="a9850-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9850-137">RELATED LINKS</span></span>

[<span data-ttu-id="a9850-138">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="a9850-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


