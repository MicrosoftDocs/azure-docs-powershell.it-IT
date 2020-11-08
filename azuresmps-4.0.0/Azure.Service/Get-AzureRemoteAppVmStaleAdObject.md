---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023588"
---
# <span data-ttu-id="e5b62-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="e5b62-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="e5b62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5b62-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b62-103">Ottiene gli oggetti in Azure Active Directory associati alle macchine virtuali di Azure RemoteApp che non esistono più.</span><span class="sxs-lookup"><span data-stu-id="e5b62-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="e5b62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5b62-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e5b62-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5b62-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b62-106">Il cmdlet **Get-AzureRemoteAppVmStaleAdObject** ottiene gli oggetti in Azure Active Directory associati alle macchine virtuali di Azure RemoteApp che non esistono più.</span><span class="sxs-lookup"><span data-stu-id="e5b62-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="e5b62-107">Questo cmdlet Visualizza il nome di ogni oggetto che viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="e5b62-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="e5b62-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5b62-108">EXAMPLES</span></span>

### <span data-ttu-id="e5b62-109">Esempio 1: ottenere oggetti non aggiornati per una raccolta</span><span class="sxs-lookup"><span data-stu-id="e5b62-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="e5b62-110">Questo secondo comando ottiene gli oggetti non aggiornati per la raccolta denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="e5b62-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="e5b62-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5b62-111">PARAMETERS</span></span>

### <span data-ttu-id="e5b62-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e5b62-112">-CollectionName</span></span>
<span data-ttu-id="e5b62-113">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5b62-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="e5b62-114">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="e5b62-114">-Credential</span></span>
<span data-ttu-id="e5b62-115">Specifica una credenziale con diritti per eseguire questa azione.</span><span class="sxs-lookup"><span data-stu-id="e5b62-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="e5b62-116">Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="e5b62-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="e5b62-117">Se non specifichi questo parametro, questo cmdlet usa le credenziali utente correnti.</span><span class="sxs-lookup"><span data-stu-id="e5b62-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

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

### <span data-ttu-id="e5b62-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="e5b62-118">-Profile</span></span>
<span data-ttu-id="e5b62-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5b62-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5b62-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e5b62-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5b62-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b62-121">CommonParameters</span></span>
<span data-ttu-id="e5b62-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b62-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b62-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5b62-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b62-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5b62-124">INPUTS</span></span>

## <span data-ttu-id="e5b62-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5b62-125">OUTPUTS</span></span>

### <span data-ttu-id="e5b62-126">Stringa</span><span class="sxs-lookup"><span data-stu-id="e5b62-126">String</span></span>

## <span data-ttu-id="e5b62-127">Note</span><span class="sxs-lookup"><span data-stu-id="e5b62-127">NOTES</span></span>

## <span data-ttu-id="e5b62-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5b62-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5b62-129">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="e5b62-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


