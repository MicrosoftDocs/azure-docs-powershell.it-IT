---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023641"
---
# <span data-ttu-id="84c06-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="84c06-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="84c06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84c06-102">SYNOPSIS</span></span>
<span data-ttu-id="84c06-103">Consente l'accesso desktop remoto a un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="84c06-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="84c06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84c06-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84c06-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84c06-105">DESCRIPTION</span></span>
<span data-ttu-id="84c06-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="84c06-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="84c06-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="84c06-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="84c06-108">Il cmdlet **Enable-AzureServiceProjectRemoteDesktop** consente l'accesso desktop remoto a un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="84c06-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="84c06-109">Per rendere effettive le modifiche, è necessario pubblicare il servizio usando il cmdlet **Publish-AzureServiceProject** dopo l'abilitazione dell'accesso desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="84c06-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="84c06-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84c06-110">EXAMPLES</span></span>

## <span data-ttu-id="84c06-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84c06-111">PARAMETERS</span></span>

### <span data-ttu-id="84c06-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84c06-112">-PassThru</span></span>
<span data-ttu-id="84c06-113">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="84c06-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84c06-114">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="84c06-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="84c06-115">-Password</span><span class="sxs-lookup"><span data-stu-id="84c06-115">-Password</span></span>
<span data-ttu-id="84c06-116">Specifica la password.</span><span class="sxs-lookup"><span data-stu-id="84c06-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c06-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="84c06-117">-Profile</span></span>
<span data-ttu-id="84c06-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84c06-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84c06-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="84c06-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="84c06-120">-Username</span><span class="sxs-lookup"><span data-stu-id="84c06-120">-Username</span></span>
<span data-ttu-id="84c06-121">Specifica il nome utente da usare per la connessione all'istanza del ruolo in Azure tramite il protocollo RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="84c06-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c06-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c06-122">CommonParameters</span></span>
<span data-ttu-id="84c06-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84c06-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c06-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84c06-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c06-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84c06-125">INPUTS</span></span>

## <span data-ttu-id="84c06-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84c06-126">OUTPUTS</span></span>

## <span data-ttu-id="84c06-127">Note</span><span class="sxs-lookup"><span data-stu-id="84c06-127">NOTES</span></span>

## <span data-ttu-id="84c06-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84c06-128">RELATED LINKS</span></span>

[<span data-ttu-id="84c06-129">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="84c06-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="84c06-130">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="84c06-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


