---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029554"
---
# <span data-ttu-id="88742-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="88742-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="88742-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88742-102">SYNOPSIS</span></span>
<span data-ttu-id="88742-103">Rimuove un endpoint da un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="88742-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="88742-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88742-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="88742-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88742-105">DESCRIPTION</span></span>
<span data-ttu-id="88742-106">Il cmdlet **Remove-AzureTrafficManagerEndpoint** consente di rimuovere un endpoint da un profilo di Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="88742-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="88742-107">Dopo aver rimosso un endpoint, passare il risultato al cmdlet **set-AzureTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="88742-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88742-108">Questo cmdlet si connette a Azure per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="88742-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="88742-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88742-109">EXAMPLES</span></span>

### <span data-ttu-id="88742-110">Esempio 1: rimuovere un endpoint da un profilo</span><span class="sxs-lookup"><span data-stu-id="88742-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="88742-111">Il primo comando usa il cmdlet **Get-AzureTrafficManagerProfile** per ottenere il profilo denominato ContosoProfile e lo archivia nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="88742-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="88742-112">Il secondo comando rimuove un endpoint con il nome di dominio Contoso02App.cloudapp.net dal profilo di Traffic Manager archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="88742-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="88742-113">Il comando passa l'oggetto profile al cmdlet **set-AzureTrafficManagerProfile** per connettersi a Azure per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="88742-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="88742-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88742-114">PARAMETERS</span></span>

### <span data-ttu-id="88742-115">-DomainName</span><span class="sxs-lookup"><span data-stu-id="88742-115">-DomainName</span></span>
<span data-ttu-id="88742-116">Specifica il nome di dominio dell'endpoint da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="88742-116">Specifies the domain name of the endpoint to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88742-117">-Force</span><span class="sxs-lookup"><span data-stu-id="88742-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88742-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="88742-118">-Profile</span></span>
<span data-ttu-id="88742-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88742-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="88742-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="88742-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88742-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88742-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="88742-122">Specifica l'oggetto profilo Traffic Manager da cui rimuovere l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="88742-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88742-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88742-123">CommonParameters</span></span>
<span data-ttu-id="88742-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88742-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88742-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88742-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88742-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88742-126">INPUTS</span></span>

## <span data-ttu-id="88742-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88742-127">OUTPUTS</span></span>

### <span data-ttu-id="88742-128">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="88742-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="88742-129">Questo cmdlet genera un oggetto profilo di Traffic Manager, che contiene informazioni sul profilo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="88742-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="88742-130">Note</span><span class="sxs-lookup"><span data-stu-id="88742-130">NOTES</span></span>

## <span data-ttu-id="88742-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88742-131">RELATED LINKS</span></span>

[<span data-ttu-id="88742-132">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="88742-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="88742-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="88742-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="88742-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88742-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="88742-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="88742-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


